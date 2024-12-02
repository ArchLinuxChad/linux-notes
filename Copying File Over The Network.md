# Copying File Over The Network

## Using `scp`

```
scp /path/to/file host:/path/for/file
```

## Using `Net Cat`

### On Host

```
nc -l <port number> < /path/to/file
```

### On client

```
nc host <port number> > /path/for/file
```

## Using Rsync

```
rsync /path/to/file host:/path/for/file
```