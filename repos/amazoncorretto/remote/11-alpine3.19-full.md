## `amazoncorretto:11-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:70635437de68bd072d44697094596d82d0ed52e72f30ec5eb97338a5252eda81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b70601b23cf59662cc16d941c14e45d1700adc9b0b4b742fc1045665c9241f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145330637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0831668f5cb1f2f5317ff5c319b5d61fa21418f5d383e278b904b4ab6a83e408`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c234dd1f0839ed6183e7d592e69800688a102718c04046ae02ecc4f866827466`  
		Last Modified: Wed, 08 Jan 2025 18:10:17 GMT  
		Size: 141.9 MB (141910395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0137d9baf422e90eb6c1de22e392246631b3149b2553c8e9826e8c341cafec9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 KB (397110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2d8c3a1cf2f7277d41dc7399e241169f3fce4561daedd49cde3614b57eb64d`

```dockerfile
```

-	Layers:
	-	`sha256:cacdd67a0a37fee9582a9744876d2f84e5b158b5ff39981b2c9d51ef3ba39669`  
		Last Modified: Wed, 08 Jan 2025 18:10:15 GMT  
		Size: 387.7 KB (387693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b951db44d3797885d26a3d70f7ffd4aa6dde011c17dabd2601f426e1b3c6b063`  
		Last Modified: Wed, 08 Jan 2025 18:10:15 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:02260815a4d231d0325b949407e9e9de9a641e069698fd332ae5c88973c64c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143383143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68b0849392297c55289ebf3cf2f30a1b1395eada685d5432b1dfc95c23f4c1d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.5-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f2178dde0fb65be0d15359886bb642d5d8dac86ca2d709ab90f8f0ee62211ca2`  
		Last Modified: Tue, 07 Jan 2025 03:03:15 GMT  
		Size: 3.4 MB (3351948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4842989fc6f6d86ba8bbda5512e7c979efaf7009e63e415341648b3e866f2b01`  
		Last Modified: Tue, 07 Jan 2025 07:22:04 GMT  
		Size: 140.0 MB (140031195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e213bb70251aff67e6b8fdd662a1a8e7567f17322b4159df74c374b29f53ce99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.3 KB (397270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92431636dde958422a4222ceaa806e0bdb11d1fc642bb35246a6df7f3d4209ec`

```dockerfile
```

-	Layers:
	-	`sha256:4d283c61e630fafa9de258e3336e6a7fa415dcf8078f0e059a4ee7d2fb7acdcc`  
		Last Modified: Tue, 07 Jan 2025 07:21:59 GMT  
		Size: 387.7 KB (387749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7711ff8d4d36500b181b461f5d527cef874a828e94eb55fb6692ecf4d494082`  
		Last Modified: Tue, 07 Jan 2025 07:21:59 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
