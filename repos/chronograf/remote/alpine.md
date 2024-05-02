## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:d11a629d4cfa1e0b9ca605f0719d5a9dc17add74c6fa2ed5f1901d2cb5c88be8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:bfdc2916cdf18901c104cbb5f9c37af0dcc9670c7da181038e306ff77d6cd169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31589712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8161dc609b83d7c07ff98e4828ced9b2e7f2ca0ff7144adade754fc64e7b28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68e27f81705183aede5ec8d16b05af8c07d462f75e94160d798299e372f7a69`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310f07ece82e275ea4dc66a9a9033fdcdaf998fe6c7997781d299f934b8c039f`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 295.8 KB (295755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df60bc3d01a0c01b095244792c5eb913e78e49a27aed12d0298bfeb99e8a5ae0`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 27.9 MB (27866708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809a3d10431465aa989b32320fcfa614917e4dd78b0ef3b4ba628af38b03e71c`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26c5e66ed649fcbf21fdb6804855736c49214b33b70c57c236a56a02a0571a`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cb52b403bfe177c53c218fda5245ba026945a8f393b97742e454946cf636a0`  
		Last Modified: Wed, 01 May 2024 21:52:23 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:d9169b4cb482ee5951ad4ecd2517a3d1409300a9dbb434cf060738a8755d0638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 KB (248883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1186269e1898e56e2c477e1d1b6f8cdc68fa2be6a7ec7f5d9d857d8ac776419e`

```dockerfile
```

-	Layers:
	-	`sha256:f971f5ac4f8155c9092387ba6239303ff77b238f4abcfaaf23311628c0c78175`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 231.1 KB (231128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9504ad10dc79d5f0656c0ac6e2b5636b26abca0889311e5b247b31f93728d9cc`  
		Last Modified: Wed, 01 May 2024 21:52:22 GMT  
		Size: 17.8 KB (17755 bytes)  
		MIME: application/vnd.in-toto+json
