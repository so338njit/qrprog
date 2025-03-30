# QR Code Generator

A simple Python application that generates QR codes from URLs.

## Default QR Code

The QR code below is generated from the default URL specified in the application:

![QR Code](qr_codes/readme_qr.png)

## Usage

### Running with Docker

Build the Docker image:
```bash
docker build -t githomeqr .
```

Run the container with volume mount to save QR codes to your local machine:
```bash
docker run -v $(pwd)/qr_codes:/app/qr_codes githomeqr
```

You can specify a custom URL:
```bash
docker run -v $(pwd)/qr_codes:/app/qr_codes githomeqr --url "https://example.com"
```

## Environment Variables

The application can be configured with the following environment variables:

- `QR_CODE_DIR`: Directory where QR codes are saved (default: `qr_codes`)
- `FILL_COLOR`: Fill color for the QR code (default: `red`)
- `BACK_COLOR`: Background color for the QR code (default: `white`)

You can set these in a `.env` file or pass them when running the container.
# QR Code Generator

A simple Python application that generates QR codes from URLs.

## Sample QR Code

![QR Code](qr_codes/QRCode_TIMESTAMP.png)

*Note: The timestamp in the filename will be different for you. Replace "QRCode_TIMESTAMP.png" with the actual filename that was generated.*

## Usage

### Running with Docker

Build the Docker image:
```bash
docker build -t githomeqr .
```

Run the container:
```bash
docker run -v $(pwd)/qr_codes:/app/qr_codes githomeqr
```

You can specify a custom URL:
```bash
docker run -v $(pwd)/qr_codes:/app/qr_codes githomeqr --url "https://example.com"
```