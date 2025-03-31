# [WatchYoBack](https://music.apple.com/cz/song/watch-your-back/1434528725)

## About The Project

A simple tool to watch a git repository for changes.

## Getting Started

### Prerequisites

* Python 3.10 =<
* Git installed

### Installation

1. Clone the repo
    ```sh
    git clone https://github.com/BakaSuspeitinho/watchyoback.git
    ```

## Usage

```sh
python watchyoback /path/to/repository --action "your-command-here"
```

### Arguments

- `repo_path`: Path to the Git repository to watch (required)
- `--action`, `-a`: Command to run when changes are detected (optional)
- `--interval`, `-i`: Polling interval in seconds (default: 10)
- `--no-pull`, `-n`: Disable automatic git pull
- `--log-level`, `-l`: Set logging level (DEBUG, INFO, WARNING, ERROR, CRITICAL)

### Examples

Basic usage (check for changes every 10 seconds):
```sh
python watchyoback /path/to/repo
```

Run action when changes are detected:
```sh
python watchyoback /path/to/repo --action "echo 'watch your back'"
```

## Roadmap

- [x] Watches for changes
- [x] Run action when changes detected
- [ ] Rollback when action fails
- [ ] Only run action after CI/CD passes