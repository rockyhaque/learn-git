# Retrieving Git Configuration Values

Git allows you to retrieve specific configuration values using the `--get` flag. This is useful when you want to access a single value from your Git configuration without listing all the settings. In this lesson, you'll learn how to use the `--get` flag to retrieve a specific configuration value.

---

## How to Retrieve a Configuration Value

To retrieve a specific configuration value, use the following syntax:

```bash
git config --get <key>
```

### Example:

```bash
git config --get user.name
```

This command retrieves the value of the `user.name` key from your Git configuration.

---

## Assignment: Retrieve a Custom Configuration Value

In this assignment, you'll retrieve the value of the `webflyx.valuation` key from the local Git configuration of the `Webflyx` repository.

1. **Retrieve the Value:**  
   Use the `--get` flag to retrieve the value of the `webflyx.valuation` key:

   ```bash
   git config --get webflyx.valuation
   ```

   This will output the value `mid`, which you set earlier.

---

## Example Output

When you run the command, you'll see output similar to this:

```
mid
```

---

## Why Use `--get`?

- **Efficiency:** Retrieve a single value without listing all configuration settings.
- **Scripting:** Useful in scripts or automation where you need to access specific configuration values.
- **Debugging:** Quickly check the value of a specific key to diagnose issues.

---
