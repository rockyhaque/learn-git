# Handling Duplicate Keys in Git Configuration

Git allows you to store **duplicate keys** in its configuration, which is unusual for a key-value store. This means you can have multiple values for the same key. However, this can lead to confusion, so Git provides the `--unset-all` flag to remove all instances of a key at once. In this lesson, you'll learn how to handle duplicate keys and use the `--unset-all` flag to clean up your configuration.

---

## How to Add Duplicate Keys

To add multiple values for the same key, use the `--add` flag:

```bash
git config --add <key> "<value>"
```

### Example:

```bash
git config --add webflyx.ceo "Warren"
git config --add webflyx.ceo "Carson"
git config --add webflyx.ceo "Sarah"
```

This adds three values for the `webflyx.ceo` key.

---

## Viewing Duplicate Keys

To view all configuration values, including duplicates, use the `--list` flag:

```bash
git config --list --local
```

### Example Output:

```
webflyx.ceo=Warren
webflyx.ceo=Carson
webflyx.ceo=Sarah
```

---

## Removing All Instances of a Key

To remove all instances of a key, use the `--unset-all` flag:

```bash
git config --unset-all <key>
```

### Example:

```bash
git config --unset-all webflyx.ceo
```

This removes all values for the `webflyx.ceo` key.

---

## Assignment: Handle Duplicate Keys

In this assignment, you'll add multiple CEOs to the `Webflyx` configuration, view the duplicates, and then remove them all at once.

1. **Add Multiple CEOs:**  
   Add three CEOs to the `webflyx.ceo` key:

   ```bash
   git config --add webflyx.ceo "Warren"
   git config --add webflyx.ceo "Carson"
   git config --add webflyx.ceo "Sarah"
   ```

2. **View the Configuration:**  
   Use the `--list --local` flag to view the configuration:

   ```bash
   git config --list --local
   ```

   You should see multiple entries for the `webflyx.ceo` key.

3. **Remove All CEOs:**  
   Use the `--unset-all` flag to remove all instances of the `webflyx.ceo` key:

   ```bash
   git config --unset-all webflyx.ceo
   ```

4. **Verify the Removal:**  
   Use the `--list --local` flag again to verify that all `webflyx.ceo` entries have been removed:
   ```bash
   git config --list --local
   ```

---

## Example Output

After adding the CEOs, the output of `git config --list --local` might look like this:

```
webflyx.ceo=Warren
webflyx.ceo=Carson
webflyx.ceo=Sarah
```

After removing the CEOs, the output will no longer include the `webflyx.ceo` key.

---

## Why Use `--unset-all`?

- **Clean Up Duplicates:** Remove all instances of a key when duplicates are no longer needed.
- **Avoid Confusion:** Ensure that your configuration is clear and free of unexpected duplicates.
- **Debugging:** Fix issues caused by duplicate or conflicting configuration values.
