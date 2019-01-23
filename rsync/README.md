# `rsync` for GitHub Actions

## Usage

To use the action simply add the following lines to your `.github/main.workflow`

```
action "Sync files" {
  uses = "mthenw/actions/rsync@master"
  args = "-avzh build/"
  secrets = [
    "PRIVATE_KEY",
    "PUBLIC_KEY",
    "USER",
    "HOST",
    "TARGET_PATH"
  ]
}
```

### Required Arguments

The argument you will use is the argument passed to `rsync` command. You should exclude target server and path from it and pass them as secrets.

### Required Secrets

You'll need to provide some secrets to use the action.

* **PRIVATE_KEY**: Your SSH private key.
* **PUBLIC_KEY**: Your SSH public key.
* **HOST**: The target host  ie, `your.site.com`.
* **USER**: The user the SSH command will auth as with the public key.
* **TARGET_PATH**: The path that files will be synced to
