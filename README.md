# Gollum dark theme

## Usage

### Gollum

Create file `custom.css` in wiki root and start gollum with option `-css`

### Nginx

Add in Nginx vhost config sub_filter

```conf
server {
    listen          80;
    ...

    location / {
        ...
        '</head>'
        '<link rel="stylesheet" type="text/css" href="http://127.0.0.1:8081/custom.css">
        </head>';
        sub_filter_once on;
        ...
    }
}
```