# Visual Studio Code Language Packs

Visual Studio Code is localized into many different languages using the concept of Language Packs. Language Packs can be installed by running the `>Configure Display Language` command in Visual Studio Code's Command Palette or installed via the [Visual Studio Code Marketplace](https://marketplace.visualstudio.com/search?target=VSCode&category=Language%20Packs&sortBy=Installs).

The original English strings can be found in the source code of the [open source repository](https://github.com/microsoft/vscode), and the localized strings for supported languages can be found in this repository.

Localized resource files are managed and edited by Microsoft. Files will be exported to this repository when strings are updated to prepare for the publishing of language packs.

There are currently 14 supported languages for Visual Studio Code.

|Language|Visual Studio Code Language ID|MLCP Language Code|
|--------|--------|--------|
|**French**|fr|French (fr-fr)
|**Italian**|it|Italian (it-it)
|**German**|de|German (de-de)
|**Spanish**|es|Spanish (es-es)
|**Russian**|ru|Russian (ru-ru)
|**Chinese (Simplified)**|zh-cn|Chinese Simplified (zh-cn)
|**Chinese (Traditional)**|zh-tw|Chinese Traditional (zh-tw)
|**Japanese**|ja|Japanese (ja-jp)
|**Korean**|ko|Korean (ko-kr)
|**Czech**|cs|Czech (cs-CZ)
|**Portuguese (Brazil)**|pt-br|Portuguese (Brazil) (pt-br)
|**Turkish**|tr|Turkish (tr-tr)
|**Polish**|pl|Polish (pl-pl)
|**Pseudo Language**|qps-ploc|Pseudo (qps-ploc)

## Contributing

If you want to give feedback or report an issue with a translation, please create a [new GitHub issue](https://github.com/microsoft/vscode-loc/issues/new). Please check if a topic about your issue already exists!
Translation strings are managed on the Microsoft Localization Platform, and changes to strings can only be made there. Consequently, pull requests fixing translations won't be accepted. All other PRs to things like `README.md`, `package.json`, etc., will be accepted at the discretion of the maintainers.

## Legal

Before we can accept your pull request, you will need to sign a **Contribution License Agreement**. All you need to do is submit a pull request. It will then be appropriately labeled (e.g., `cla-required`, `cla-norequired`, `cla-signed`, `cla-already-signed`). If you already signed the agreement, we will continue with reviewing the PR; otherwise, our system will tell you how you can sign the CLA. Once you sign the CLA, all future PRs will be labeled as `cla-signed`.

# Microsoft Open Source Code of Conduct

This project has adopted the [**Microsoft Open Source Code of Conduct**](https://opensource.microsoft.com/codeofconduct/).
For more information, see the [**Code of Conduct FAQ**](https://opensource.microsoft.com/codeofconduct/faq/) or contact [**opencode@microsoft.com**](mailto:opencode@microsoft.com) with any additional questions or comments.

## License

[MIT](LICENSE.md)
brew install --cask github-copilot-for-xcode            - name: Cache
  uses: actions/cache@v5.0.3
  with:
    # A list of files, directories, and wildcard patterns to cache and restore
    path: 
    # An explicit key for restoring and saving the cache
    key: 
    # An ordered multiline string listing the prefix-matched keys, that are used for restoring stale cache if no cache hit occurred for key. Note `cache-hit` returns false in this case.
    restore-keys: # optional
    # The chunk size used to split up large files during upload, in bytes
    upload-chunk-size: # optional
    # An optional boolean when enabled, allows windows runners to save or restore caches that can be restored or saved respectively on other platforms
    enableCrossOsArchive: # optional, default is false
    # Fail the workflow if cache entry is not found
    fail-on-cache-miss: # optional, default is false
    # Check if a cache entry exists for the given input(s) (key, restore-keys) without downloading the cache
    lookup-only: # optional, default is false
    # Run the post step to save the cache even if another step before fails
    save-always: # optional, default is false
                      - name: Download a Build Artifact
  uses: actions/download-artifact@v8.0.1
  with:
    # Name of the artifact to download. If unspecified, all artifacts for the run are downloaded.
    name: # optional
    # IDs of the artifacts to download, comma-separated. Either inputs `artifact-ids` or `name` can be used, but not both.
    artifact-ids: # optional
    # Destination path. Supports basic tilde expansion. Defaults to $GITHUB_WORKSPACE
    path: # optional
    # A glob pattern matching the artifacts that should be downloaded. Ignored if name is specified.
    pattern: # optional
    # When multiple artifacts are matched, this changes the behavior of the destination directories. If true, the downloaded artifacts will be in the same directory specified by path. If false, the downloaded artifacts will be extracted into individual named directories within the specified path.
    merge-multiple: # optional, default is false
    # The GitHub token used to authenticate with the GitHub API. This is required when downloading artifacts from a different repository or from a different workflow run. If this is not specified, the action will attempt to download artifacts from the current repository and the current workflow run.
    github-token: # optional
    # The repository owner and the repository name joined together by "/". If github-token is specified, this is the repository that artifacts will be downloaded from.
    repository: # optional, default is ${{ github.repository }}
    # The id of the workflow run where the desired download artifact was uploaded from. If github-token is specified, this is the run that artifacts will be downloaded from.
    run-id: # optional, default is ${{ github.run_id }}
    # If true, the downloaded artifact will not be automatically extracted/decompressed. This is useful when you want to handle the artifact as-is without extraction.
    skip-decompress: # optional, default is false
    # The behavior when a downloaded artifact's digest does not match the expected digest. Options: ignore, info, warn, error. Default is error which will fail the action.
    digest-mismatch: # optional, default is error
                      - name: Setup Go environment
  uses: actions/setup-go@v6.3.0
  with:
    # The Go version to download (if necessary) and use. Supports semver spec and ranges. Be sure to enclose this option in single quotation marks.
    go-version: # optional
    # Path to the go.mod, go.work, .go-version, or .tool-versions file.
    go-version-file: # optional
    # Set this option to true if you want the action to always check for the latest available version that satisfies the version spec
    check-latest: # optional
    # Used to pull Go distributions from go-versions. Since there's a default, this is typically not supplied by the user. When running this action on github.com, the default value is sufficient. When running on GHES, you can pass a personal access token for github.com if you are experiencing rate limiting.
    token: # optional, default is ${{ github.server_url == 'https://github.com' && github.token || '' }}
    # Used to specify whether caching is needed. Set to true, if you'd like to enable caching.
    cache: # optional, default is true
    # Used to specify the path to a dependency file (e.g., go.mod, go.sum)
    cache-dependency-path: # optional
    # Target architecture for Go to use. Examples: x86, x64. Will use system architecture by default.
    architecture: # optional
                      - name: Close Stale Issues
  uses: actions/stale@v10.2.0
  with:
    # Token for the repository. Can be passed in using `{{ secrets.GITHUB_TOKEN }}`.
    repo-token: # optional, default is ${{ github.token }}
    # The message to post on the issue when tagging it. If none provided, will not mark issues stale.
    stale-issue-message: # optional
    # The message to post on the pull request when tagging it. If none provided, will not mark pull requests stale.
    stale-pr-message: # optional
    # The message to post on the issue when closing it. If none provided, will not comment when closing an issue.
    close-issue-message: # optional
    # The message to post on the pull request when closing it. If none provided, will not comment when closing a pull requests.
    close-pr-message: # optional
    # The number of days old an issue or a pull request can be before marking it stale. Set to -1 to never mark issues or pull requests as stale automatically.
    days-before-stale: # optional, default is 60
    # The number of days old an issue can be before marking it stale. Set to -1 to never mark issues as stale automatically. Override "days-before-stale" option regarding only the issues.
    days-before-issue-stale: # optional
    # The number of days old a pull request can be before marking it stale. Set to -1 to never mark pull requests as stale automatically. Override "days-before-stale" option regarding only the pull requests.
    days-before-pr-stale: # optional
    # The number of days to wait to close an issue or a pull request after it being marked stale. Set to -1 to never close stale issues or pull requests.
    days-before-close: # optional, default is 7
    # The number of days to wait to close an issue after it being marked stale. Set to -1 to never close stale issues. Override "days-before-close" option regarding only the issues.
    days-before-issue-close: # optional
    # The number of days to wait to close a pull request after it being marked stale. Set to -1 to never close stale pull requests. Override "days-before-close" option regarding only the pull requests.
    days-before-pr-close: # optional
    # The label to apply when an issue is stale.
    stale-issue-label: # optional, default is Stale
    # The label to apply when an issue is closed.
    close-issue-label: # optional
    # The labels that mean an issue is exempt from being marked stale. Separate multiple labels with commas (eg. "label1,label2").
    exempt-issue-labels: # optional, default is 
    # The reason to use when closing an issue.
    close-issue-reason: # optional, default is not_planned
    # The label to apply when a pull request is stale.
    stale-pr-label: # optional, default is Stale
    # The label to apply when a pull request is closed.
    close-pr-label: # optional
    # The labels that mean a pull request is exempt from being marked as stale. Separate multiple labels with commas (eg. "label1,label2").
    exempt-pr-labels: # optional, default is 
    # The milestones that mean an issue or a pull request is exempt from being marked as stale. Separate multiple milestones with commas (eg. "milestone1,milestone2").
    exempt-milestones: # optional, default is 
    # The milestones that mean an issue is exempt from being marked as stale. Separate multiple milestones with commas (eg. "milestone1,milestone2"). Override "exempt-milestones" option regarding only the issues.
    exempt-issue-milestones: # optional, default is 
    # The milestones that mean a pull request is exempt from being marked as stale. Separate multiple milestones with commas (eg. "milestone1,milestone2"). Override "exempt-milestones" option regarding only the pull requests.
    exempt-pr-milestones: # optional, default is 
    # Exempt all issues and pull requests with milestones from being marked as stale. Default to false.
    exempt-all-milestones: # optional, default is false
    # Exempt all issues with milestones from being marked as stale. Override "exempt-all-milestones" option regarding only the issues.
    exempt-all-issue-milestones: # optional, default is 
    # Exempt all pull requests with milestones from being marked as stale. Override "exempt-all-milestones" option regarding only the pull requests.
    exempt-all-pr-milestones: # optional, default is 
    # Only issues or pull requests with all of these labels are checked if stale. Defaults to `` (disabled) and can be a comma-separated list of labels.
    only-labels: # optional, default is 
    # Only issues or pull requests with at least one of these labels are checked if stale. Defaults to `` (disabled) and can be a comma-separated list of labels.
    any-of-labels: # optional, default is 
    # Only issues with at least one of these labels are checked if stale. Defaults to `` (disabled) and can be a comma-separated list of labels. Override "any-of-labels" option regarding only the issues.
    any-of-issue-labels: # optional, default is 
    # Only pull requests with at least one of these labels are checked if stale. Defaults to `` (disabled) and can be a comma-separated list of labels. Override "any-of-labels" option regarding only the pull requests.
    any-of-pr-labels: # optional, default is 
    # Only issues with all of these labels are checked if stale. Defaults to `[]` (disabled) and can be a comma-separated list of labels. Override "only-labels" option regarding only the issues.
    only-issue-labels: # optional, default is 
    # Only pull requests with all of these labels are checked if stale. Defaults to `[]` (disabled) and can be a comma-separated list of labels. Override "only-labels" option regarding only the pull requests.
    only-pr-labels: # optional, default is 
    # The maximum number of operations per run, used to control rate limiting (GitHub API CRUD related).
    operations-per-run: # optional, default is 30
    # Remove stale labels from issues and pull requests when they are updated or commented on.
    remove-stale-when-updated: # optional, default is true
    # Remove stale labels from issues when they are updated or commented on. Override "remove-stale-when-updated" option regarding only the issues.
    remove-issue-stale-when-updated: # optional, default is 
    # Remove stale labels from pull requests when they are updated or commented on. Override "remove-stale-when-updated" option regarding only the pull requests.
    remove-pr-stale-when-updated: # optional, default is 
    # Run the processor in debug mode without actually performing any operations on live issues.
    debug-only: # optional, default is false
    # The order to get issues or pull requests. Defaults to false, which is descending.
    ascending: # optional, default is false
    # What to sort results by. Valid options are `created`, `updated`, and `comments`. Defaults to `created`.
    sort-by: # optional, default is created
    # Delete the git branch after closing a stale pull request.
    delete-branch: # optional, default is false
    # The date used to skip the stale action on issue/pull request created before it (ISO 8601 or RFC 2822).
    start-date: # optional, default is 
    # The assignees which exempt an issue or a pull request from being marked as stale. Separate multiple assignees with commas (eg. "user1,user2").
    exempt-assignees: # optional, default is 
    # The assignees which exempt an issue from being marked as stale. Separate multiple assignees with commas (eg. "user1,user2"). Override "exempt-assignees" option regarding only the issues.
    exempt-issue-assignees: # optional, default is 
    # The assignees which exempt a pull request from being marked as stale. Separate multiple assignees with commas (eg. "user1,user2"). Override "exempt-assignees" option regarding only the pull requests.
    exempt-pr-assignees: # optional, default is 
    # Exempt all issues and pull requests with assignees from being marked as stale. Default to false.
    exempt-all-assignees: # optional, default is false
    # Exempt all issues with assignees from being marked as stale. Override "exempt-all-assignees" option regarding only the issues.
    exempt-all-issue-assignees: # optional, default is 
    # Exempt all pull requests with assignees from being marked as stale. Override "exempt-all-assignees" option regarding only the pull requests.
    exempt-all-pr-assignees: # optional, default is 
    # Exempt draft pull requests from being marked as stale. Default to false.
    exempt-draft-pr: # optional, default is false
    # Display some statistics at the end regarding the stale workflow (only when the logs are enabled).
    enable-statistics: # optional, default is true
    # A comma delimited list of labels to add when an issue or pull request becomes unstale.
    labels-to-add-when-unstale: # optional, default is 
    # A comma delimited list of labels to remove when an issue or pull request becomes stale.
    labels-to-remove-when-stale: # optional, default is 
    # A comma delimited list of labels to remove when an issue or pull request becomes unstale.
    labels-to-remove-when-unstale: # optional, default is 
    # Any update (update/comment) can reset the stale idle time on the issues and pull requests.
    ignore-updates: # optional, default is false
    # Any update (update/comment) can reset the stale idle time on the issues. Override "ignore-updates" option regarding only the issues.
    ignore-issue-updates: # optional, default is 
    # Any update (update/comment) can reset the stale idle time on the pull requests. Override "ignore-updates" option regarding only the pull requests.
    ignore-pr-updates: # optional, default is 
    # Only the issues or the pull requests with an assignee will be marked as stale automatically.
    include-only-assigned: # optional, default is false
    # Only issues with a matching type are processed as stale/closed. Defaults to `[]` (disabled) and can be a comma-separated list of issue types.
    only-issue-types: # optional, default is 
          FORCE_JAVASCRIPT_ACTIONS_TO_NODE24=true.env
