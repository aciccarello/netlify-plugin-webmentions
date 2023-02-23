# Netlify Build Plugin: Automatically discover any webmentions and send them after every production build

> **Note:** This is a fork of the [netlify-plugin-webmentions](https://github.com/CodeFoodPixels/netlify-plugin-webmentions) repo

Automatically discover any webmentions and send them after every production build.

This plugin will send webmentions to any mentioned websites that have a webmention endpoint after every production build. The plugin can be used without any configuration if using the defaults.

## Usage

### File based installation
To use file based installation, add this package to your `devDependencies`: 

```
npm install -D @aciccarello/netlify-plugin-webmentions
```

Then add the following lines to your `netlify.toml` file:

```toml
[[plugins]]
  package = "@aciccarello/netlify-plugin-webmentions"

	[plugins.inputs]

	# The base url of your site (optional, default: main URL set in Netlify)
	baseUrl = "https://example.com"

	# Path to the feed URL (optional, default: /feed.xml)
	feedPath = "/feed.xml"

	# Maximum number of feed entries to check for mentions (optional, default: 1)
	limit = 1
```

Note: The `[[plugins]]` line is required for each plugin, even if you have other plugins in your `netlify.toml` file already.
