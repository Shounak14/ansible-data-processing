Ansible Data Processing Playbooks

This repository contains a set of Ansible playbooks for practicing data processing, JSON handling, and basic automation tasks. These playbooks demonstrate common Ansible concepts such as loops, conditionals, JSON parsing, merging, filtering, and summarizing data.


| Playbook                    | Description                                                                                                  |
| --------------------------- | ------------------------------------------------------------------------------------------------------------ |
| `condition_playbook.yml`    | Prints user names where age > 30 from `condition.json`.                                                      |
| `count_playbook.yml`        | Counts users with age ≥ 28 from `condition.json`.                                                            |
| `exp-output_playbook.yml`   | Converts `payload.json` into a summarized format including total orders, total money spent, and order IDs.   |
| `first_playbook.yml`        | Calculates total amount spent across all orders in `payload.json`.                                           |
| `list_playbook.yml`         | Prints a list of all order IDs from `orders.json`.                                                           |
| `merge_playbook.yml`        | Reads and merges multiple JSON files (`file1.json`, `file2.json`, `file3.json`) and removes duplicates.      |
| `nested_playbook.yml`       | Prints nested JSON data (`nested.json`) such as employee city info.                                          |
| `nested1_playbook.yml`      | Prints detailed info for each employee in `nested1.json` including city and order count.                     |
| `playbook1.yml`             | Prints full names (`first_name` + `last_name`) of users from `payload.json`.                                 |
| `pract_playbook.yml`        | Loops through a simple list of items (`bed`, `remote`, etc.) and prints them.                                |
| `sum_playbook.yml`          | Prints the sum of order amounts from `orders.json`.                                                          |
| `test_playbook.yml`         | Converts a dictionary to a list using `dict2items` and prints the values.                                    |
| `user_summary_playbook.yml` | Creates a processed summary for each user from `output.json`, including total orders and total amount spent. |



🔹 Key Concepts Demonstrated

Reading JSON files using include_vars and lookup('file', ...).

Looping over lists with loop.

Filtering data using selectattr.

Summarizing data with map, sum, length, count.

Merging multiple JSON files and removing duplicates.

Nested dictionary access in JSON.

Using set_fact to dynamically store and process data.



⚡ How to Run a Playbook

Make sure you have Ansible installed:

ansible --version


Navigate to the playbooks folder:

cd playbooks


Run a playbook using:

ansible-playbook first_playbook.yml


Replace first_playbook.yml with the playbook you want to run.



📌 Best Practices

All JSON files are stored separately for clarity.

Use {{ playbook_dir }}/../json_files/filename.json to reference JSON files from playbooks.

Sensitive data should be removed or sanitized before pushing to GitHub.

Use ansible.builtin.debug for printing intermediate values for debugging and learning purposes.
