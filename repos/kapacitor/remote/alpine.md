## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:2d30e7bbae1d8f7141df653bbb288caf9b68c7580707a0677841e7909e831017
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:a05e82cbe206d5811d18eaf53c74106a6a6b0dde9d42635437a34481e03b81c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75238393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee59970f6c741c878a3bd6f8203690c6d13048968fc100360b36870234703e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Tue, 18 Jun 2024 15:52:41 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31e1ddb58cf95dbef42c260abe85a74df05e1db6360f2993bdb9243c5449201`  
		Last Modified: Thu, 20 Jun 2024 20:56:04 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f51a3a0e428ae9d014e589a59aeb357372cc04426a5f3c2fdd548bc78a81dbb`  
		Last Modified: Thu, 20 Jun 2024 20:56:04 GMT  
		Size: 294.4 KB (294356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340ef64515d9535623b5388b0f6f760f1b50ffcce59034e0d95e5e8fe1deb692`  
		Last Modified: Thu, 20 Jun 2024 20:56:05 GMT  
		Size: 71.3 MB (71319412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f805b77f78c72be9fb4fbe19f8a9331a842e68e1c1fedce031199c08bb08b2`  
		Last Modified: Thu, 20 Jun 2024 20:56:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f6f2b9938da2c8efe8a60bfa0cb96b3a78cf1d3ef4b78589a3568731c4428a`  
		Last Modified: Thu, 20 Jun 2024 20:56:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:b1bcb60091ddf905ef8560e284d3e8fb33e514205536446db61c2da4753e2bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.6 KB (345603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9064a71ff69e0755b77525db8fcad8453b529acfe9ace4881a434b96584ec0fb`

```dockerfile
```

-	Layers:
	-	`sha256:bd1670d8ccd4e6e47e9d909340917f68a912874aa3356680db6a07fbb7dcdbed`  
		Last Modified: Thu, 20 Jun 2024 20:56:04 GMT  
		Size: 330.1 KB (330140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dfb0e1d075a395ddc74e50d8904dd9011aca1332610d97a7a95050f444a7c46`  
		Last Modified: Thu, 20 Jun 2024 20:56:04 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json
