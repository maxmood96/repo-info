## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:4b29de73901134d65fb63d43ceb169ed217a41cea0013c2ce9d356a793b43d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:32487036156063d2a292f41df2d6909ddcf587015ead7eddd26c6ff0efb6e193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75902966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b094251f0c804502e1fc81969c13c5e632d61bb3ea0d9b4682aa8ce4250ea3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 29 Sep 2025 12:39:49 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.7.7
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Wed, 08 Oct 2025 23:10:39 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0e1f91cb299838580bf7f7ef1603e455ff4b0503c7cdbfe0aebc56ff6e852a`  
		Last Modified: Tue, 09 Dec 2025 12:08:54 GMT  
		Size: 292.5 KB (292459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f05f43be72abc0195a3ec86c2ad5e5b8211b326cfbbc9bb1b4861b7e66c8e6a`  
		Last Modified: Tue, 09 Dec 2025 12:08:56 GMT  
		Size: 72.0 MB (71982671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d2c20637675d0a7793eed8d3f7a433a08a09d21ecd9ceb86ddde1d8a90d88e`  
		Last Modified: Tue, 09 Dec 2025 12:08:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f253175d5bad5565fdc8aa0837cb6151c40b8844ede1f9c2032381e64aec36`  
		Last Modified: Wed, 08 Oct 2025 23:10:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a2272f84d134db7769109c42ab599628141be6e636573dd663a13347c6fa0064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 KB (382206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c1306f8e81687ea167b0b39d7477517cca5b6b496fe11caa0ddeab5cf4363b`

```dockerfile
```

-	Layers:
	-	`sha256:3ef933bcc7ba9922e2fad7b96f23e7cc5beb964a2d4310c132b45e98d2dc09da`  
		Last Modified: Wed, 08 Oct 2025 23:10:42 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60aa5a1214558852c195c1b3f80818dbb7b1113d266e0311dddcf4f17efdb08`  
		Last Modified: Wed, 08 Oct 2025 23:10:42 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json
