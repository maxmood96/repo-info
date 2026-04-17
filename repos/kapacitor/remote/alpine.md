## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:d413cc02810588e8c459ea5be842408894d80457fd6bf3d17c76054bd4fbeba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:7dd27bf99a95c88a227895984474aed5a5acd9e005ee8c4ca5d230c5adce430d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75904570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3afb14c37dc00503a0e3d186c16cca67e6e6cf79f380e0768c83b473ab21723`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:29:59 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
ENV KAPACITOR_VERSION=1.7.7
# Fri, 17 Apr 2026 00:30:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 17 Apr 2026 00:30:05 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 17 Apr 2026 00:30:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:05 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d26afc56a247d157e5130fafb0c3e1596d90cb798a74bcd18085a2e60f5e83`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 290.8 KB (290778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62dd12f58262d16aa469c538fe54969fbd41faab46b0c454ce33250afdb5cf9`  
		Last Modified: Fri, 17 Apr 2026 00:30:19 GMT  
		Size: 72.0 MB (71982697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55baa52346461779ddbbe16b9bcbe892cdd293e258d25759833687ed332ec26f`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b697b2c16e0d0a74ce9cec7f52e70573e6c357c63cea20d805fa64c4bd2a984c`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:c43b268a38b55473ac82d1c64d91b2abf473cfd8498dadaf61b7b610b7a0a384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.5 KB (381476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c6c8a59270545d801e93fbec290d5e3507d4c0ef7d1b17af7ac1a44b9f91e2`

```dockerfile
```

-	Layers:
	-	`sha256:5e93c3927eafe526f00d32bfce704d302d02d4cbe2d4104d9f70f6c2132c0cee`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 365.8 KB (365835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d021a80b9241fd4aceb41e3907131caf439210759adcdaa248d89c1e12091d7`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 15.6 KB (15641 bytes)  
		MIME: application/vnd.in-toto+json
