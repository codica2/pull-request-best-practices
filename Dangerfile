failure 'Please fix the MR title', sticky: true unless /^\[(Feature|Fix|Hotfix|Refactor|Release)\]\s\S.*$/.match?(gitlab.mr_title)
failure 'Please add trello ticket to MR', sticky: true unless gitlab.mr_body.include?('https://trello.com/c/')
failure 'Please add labels to this MR', sticky: true if gitlab.mr_labels.empty?

warn 'This MR does not have any assignees yet.', sticky: true unless gitlab.mr_json['assignee']