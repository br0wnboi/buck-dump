# Buck-Dump

Basic AWS S3 Recon tool in Python3
Buck-Dump is a Python tool designed to quickly enumerate AWS S3 buckets, searching for potential loot. Similar to a subdomain bruteforcer, Buck-Dump is tailored specifically for S3 buckets. It comes with extra features allowing you to grep for specific files and download interesting files if you're not afraid to rapidly fill up your hard drive.

## Usage

```bash
./buck-dump.py -l <hostlist> [-D] [-d <savedir>] [-g <grepwords>] [-m <maxsize>] [-t <threads>]
```

### Options

- `-l <hostlist>`: Required. Specifies the path to the hostlist file containing a list of AWS S3 bucket names.

- `-D`: Optional. Enables the download mode, allowing the tool to save files locally.

- `-d <savedir>`: Optional. If download mode is enabled, this option allows you to specify a directory to save files. Each bucket's results will be saved in a separate directory.

- `-g <grepwords>`: Optional. Provides a wordlist file to grep for specific files within the S3 buckets.

- `-m <maxsize>`: Optional. Specifies the maximum file size to download. Default is 1024 (1 MB).

- `-t <threads>`: Optional. Specifies the number of threads to use. Default is 1.

## Features

- **Enumeration**: Buck-Dump quickly enumerates AWS S3 buckets specified in the hostlist.

- **Grep for Files**: Use the `-g` option to provide a wordlist for grepping specific files within the S3 buckets.

- **Download Mode**: Enable the `-D` option to download files from the discovered buckets. The `-d` option allows you to specify a directory for saving the downloaded files.

- **Multi-threaded**: Buck-Dump supports multi-threading to speed up the enumeration process.

## Disclaimer

Please use Buck-Dump responsibly and ensure compliance with all applicable laws and regulations. The tool is provided for educational and security testing purposes only.

## Dependencies

- Python 3
- Requests library (`pip install requests`)

## Author

[Your Name]

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
