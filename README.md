# kevin-speak

> "Me mechanic not speak English. But he know what me mean when me say 'car no go', and we best friends. So me think, why waste time say lot word when few word do trick? When me President, they see. They see."
>
> — Kevin Malone, *The Office*

A Claude Code skill that rewrites a response into Kevin's few-word English: function words gone, long words swapped for short ones, the point fully intact.

## Install

```
/plugin marketplace add ooloe/kevin-speak
/plugin install kevin-speak@kevin-speak
```

Or from a local clone:

```
/plugin marketplace add /path/to/kevin-speak
/plugin install kevin-speak@kevin-speak
```

## Use

```
/kevin-speak:kevin
```

With no arguments it rewrites the previous response. Pass text or a topic to rewrite that instead.

## Example

Before:

> I've looked at the three failing specs. The factory builds an assignment without an account, so the tenant scope filter drops the record before the query returns. You'll probably want to add the account association to the factory rather than stubbing the filter.

After:

> Me look three broken spec. Factory make assignment. No account. Scope filter throw it away. Query see nothing. Put account in factory. No stub filter.

## What it won't touch

File paths, identifiers, commands, flags, quoted code and error text, URLs, ticket keys and numbers all survive verbatim — Kevin cut his own words, not the mechanic's part numbers.

It also stays out of anything that leaves the terminal: commit messages, PR descriptions, code comments, docs and UI copy all stay in normal English. And it never shortens away a risk, a warning or a confirmation request.

## License

MIT
