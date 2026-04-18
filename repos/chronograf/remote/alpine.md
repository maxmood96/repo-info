## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:41913992a072a2fc5b7f935b05e0851f1cadb84cf0ce5e3b14ce5444905127da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c090b122c302e943ac7d72fd923b48ff169e17fbda740aac60dfa831518d5121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64549785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42e0e3604110e24dd093c463181f09858be50da21ae05d5717dc445cfff5973`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 23:11:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 23:11:15 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 23:11:21 GMT
ENV CHRONOGRAF_VERSION=1.11.1
# Fri, 17 Apr 2026 23:11:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 17 Apr 2026 23:11:21 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 17 Apr 2026 23:11:21 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 17 Apr 2026 23:11:21 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 17 Apr 2026 23:11:21 GMT
VOLUME [/var/lib/chronograf]
# Fri, 17 Apr 2026 23:11:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 23:11:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 23:11:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d762789db4e902950bb375830c4f4c99b5e4a7dd0bc04b11f6337c42a3ddd971`  
		Last Modified: Fri, 17 Apr 2026 23:11:35 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1cd6ba1ef8b8e04a45ae4016f3187f96106910e81e0c71108f7230e9580303`  
		Last Modified: Fri, 17 Apr 2026 23:11:34 GMT  
		Size: 312.2 KB (312180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5baddaa9254e37a2265eacbc7a4b1dc2a700b80fc46b81b0910cba783d39d3a6`  
		Last Modified: Fri, 17 Apr 2026 23:11:36 GMT  
		Size: 60.4 MB (60404685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a6029ead94f040b875618c5b1482280471567cc37e931256ddb5f10940fddf`  
		Last Modified: Fri, 17 Apr 2026 23:11:35 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149ba4ecbed81f5a0d71c4a36228a7358676a0318042091d57d9ebd838b22a97`  
		Last Modified: Fri, 17 Apr 2026 23:11:36 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0d4fa8934d0846ae6e80c94c8a5946666647b429e5ff0b7db401883a0118c5`  
		Last Modified: Fri, 17 Apr 2026 23:11:36 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:deed3830371624aecdcb39e815df4648f0de119cdc5a05bbd30f6b7a1a4c3a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 KB (287057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21e1c2c2004f0ee1912ce1eedda595a55d0f9016c982cf9dc72208e99479993`

```dockerfile
```

-	Layers:
	-	`sha256:74295d628b90e6849531142973a6c3f1574b2d682d0414e65814e291922813d0`  
		Last Modified: Fri, 17 Apr 2026 23:11:35 GMT  
		Size: 269.3 KB (269328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c80a873777e4bc9f51b18b07552f5cc2efc09a9e81f7a97d685a46014e3665c4`  
		Last Modified: Fri, 17 Apr 2026 23:11:34 GMT  
		Size: 17.7 KB (17729 bytes)  
		MIME: application/vnd.in-toto+json
