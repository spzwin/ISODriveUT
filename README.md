# Portable Bootable Image Creator

This tool creates portable, bootable `.img` files that can be used like USB flash drives on mobile devices.

## Features

- ✅ Creates bootable `.img` files with customizable paths
- ✅ Supports both `/documents/iso` and `/documents/flashdrive` directory structures  
- ✅ Generates read-write capable images (like real USB drives)
- ✅ Compatible with OPNsense and other system images
- ✅ Works on Linux, macOS, and Windows (via WSL)

## Usage

### Basic Usage
```bash
python create_bootable_img.py --output ./my_boot.img --size 100
```

### Custom Path
```bash
python create_bootable_img.py --output /documents/flashdrive/custom.img --size 50
```

### Full Options
```bash
python create_bootable_img.py \
  --output /path/to/output.img \
  --size 200 \
  --filesystem vfat
```

## Parameters

- `--output` (required): Output path for the .img file
- `--size` (optional, default: 100): Size in MB (50-4096 MB supported)
- `--filesystem` (optional, default: vfat): Filesystem type (vfat, ext4)

## Testing

Run the included test suite:
```bash
python test_bootable_img.py
```

## Integration

This solution integrates seamlessly with ISODriveUT by:
1. Supporting the expected directory structure (`/documents/iso`, `/documents/flashdrive`)
2. Creating properly formatted bootable images
3. Maintaining compatibility with mobile device boot requirements

## License

MIT License - Free to use and modify.