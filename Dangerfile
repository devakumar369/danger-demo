# Check 1: PR Description
warn("Please add a PR description.") if github.pr_body.nil? || github.pr_body.empty?

# Check 2: PR Title
warn("PR title should have at least 10 characters.") if github.pr_title.length < 10

# Check 3: PR Labels
warn("Please add a label to this PR.") if github.pr_labels.empty?

# Check 4: PR Size
warn("Big PR, please keep changes small.") if git.lines_of_code > 50

# Check 5: Documentation
warn("Please update README.md.") if git.modified_files.include?("calculator.py") && !git.modified_files.include?("README.md")

# Confirmation
message("Danger has completed the PR checks!")