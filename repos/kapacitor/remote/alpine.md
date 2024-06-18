## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:cae897bae6987a4b5520628e65ba26ecc19d4a444667c2e51c4910ea4c519dc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:f5bdc8925caa35843dc8f39885dd83c238c7dc9e819a13262033f0bfa8ad9203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75236644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45df85f524054e48428128a3cc971d3cedba1f0d6f17fb4b6eab3f09a11d9a55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a69d3ed5e118e2a94a15bee15eb7e9c31d16f7c1afdda9048f498847e265554`  
		Last Modified: Tue, 18 Jun 2024 18:52:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d51b6bd10ad10854f38fbaa7b6ad56f3f90ecbd36d37f814e6f640bacfd185c`  
		Last Modified: Tue, 18 Jun 2024 18:52:26 GMT  
		Size: 294.3 KB (294346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228f6efad1d99c2f46791c54265027da71bcbf9200e3bd736535c944d6315155`  
		Last Modified: Tue, 18 Jun 2024 18:52:28 GMT  
		Size: 71.3 MB (71319427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a5ea1191b19e767a8bb183c454557430f3dc3decd91ec249b07e123006192a`  
		Last Modified: Tue, 18 Jun 2024 18:52:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795182766294872d097a00665c77b063dbbf7e3810cf50cbe2e465cd71a041cd`  
		Last Modified: Tue, 18 Jun 2024 18:52:27 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:92f65d845bba4020ca688f4a6377fadfe51bf848e1861e83f04ea7f4f6da908d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.6 KB (345602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e893faad8f7c88591f1b46562a99d5bc231f5d71c9a2f9258588c49f5257718`

```dockerfile
```

-	Layers:
	-	`sha256:0eaa0dd46fef437ee9040af4def552bf57dd12b2e75cb48331dc7c492b32be9c`  
		Last Modified: Tue, 18 Jun 2024 18:52:27 GMT  
		Size: 330.1 KB (330139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:524702017e42198a7e14c6f346288c7f488d53fa45aeee66c92e191833cbc04a`  
		Last Modified: Tue, 18 Jun 2024 18:52:26 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json
