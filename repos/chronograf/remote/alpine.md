## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:3180124052084e1c0db5c3ba1bfa2f415c88fc7681ef14dfc189b324b9de03c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ee85eacf84a2662ece23a552d71cac84b11cbc3691d0f11533c47601629436a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33278682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd20a03649aab6179a8d0fbca439a20f70197cad1151f17c7db7f2bca99a7a41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jan 2026 17:54:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 07 Jan 2026 17:54:24 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 07 Jan 2026 17:54:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 07 Jan 2026 17:54:28 GMT
VOLUME [/var/lib/chronograf]
# Wed, 07 Jan 2026 17:54:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 07 Jan 2026 17:54:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Jan 2026 17:54:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb809d47327d4436ed4d3ac5b0d2b676061f267bdacedb6a6a89d360a7dae09`  
		Last Modified: Wed, 07 Jan 2026 17:54:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb19a309f7b798855a902544be3186a07abbb407e814358b58cd1b89a39f5d3b`  
		Last Modified: Wed, 07 Jan 2026 17:54:44 GMT  
		Size: 314.7 KB (314652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1806ce0ba099140396732948f565b7509ae183daafc58c9c0232df4fa0e46272`  
		Last Modified: Wed, 07 Jan 2026 17:54:38 GMT  
		Size: 29.1 MB (29136854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dad571ff7e915a85ce4aba703a3ebe307f73f0a42380e0eab5d5be6f6bc208`  
		Last Modified: Wed, 07 Jan 2026 17:54:38 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd67712f58a31ea13eee2648165a6e2c172ef5cbff62d5d29689482836291302`  
		Last Modified: Wed, 07 Jan 2026 17:54:38 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f130002e876e593ef18015df47078dcbf1e0f19cc533e5612a81b3e99b565166`  
		Last Modified: Wed, 07 Jan 2026 17:54:44 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:28567e0f67b9b9f0f79f9b8a40d1b45120c51e8222a75fbfeff2423cc7454275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 KB (269841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da3a04ba74c76ee4048ccb25b04a06ecc361c5298007bd4a37d0e9e8371a4b2`

```dockerfile
```

-	Layers:
	-	`sha256:4b9989c9337955baf604cfdcd89af7ca51dd00300557e0cb8354a7bddd10ebe2`  
		Last Modified: Wed, 07 Jan 2026 17:54:38 GMT  
		Size: 252.0 KB (252029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd5523918f180b39378a1fc48e9db5f725a139f89fcd1a1b8eae374b7001d78a`  
		Last Modified: Wed, 07 Jan 2026 19:38:29 GMT  
		Size: 17.8 KB (17812 bytes)  
		MIME: application/vnd.in-toto+json
