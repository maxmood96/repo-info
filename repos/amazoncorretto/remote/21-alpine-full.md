## `amazoncorretto:21-alpine-full`

```console
$ docker pull amazoncorretto@sha256:de29bc5a3e84652c7f475da4dc9546f5f203d545cdd15213503dfc95e5bff0e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:aa440c05bd1f9acaead6999588e5be8bdb76d196bbb0f15a9bf14966ad4c0c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165450335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02672f4dd367b7272bcb6ce9d3cf0b8a27e30bc618a6ecf51d500f3f590cb9a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:15 GMT
ARG version=21.0.10.7.1
# Wed, 21 Jan 2026 19:01:15 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:15 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3b5bdb09ad91d86c575799ac71f0f8e4cf37a35be2c5430890f6cad8a53919`  
		Last Modified: Wed, 21 Jan 2026 19:19:42 GMT  
		Size: 161.6 MB (161590231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3a0ee0b1945e6dc69f4b898a75722fe443b984558b8bcdbd7ffd4e07024dd0ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.7 KB (593722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66e3ce380bead78ae3f3836ed2daa105ac78c12d4c0d2a0be5b7d8565bae487`

```dockerfile
```

-	Layers:
	-	`sha256:26c640877ec559fad5e24943958881135967d26f7ff72eed2990490d40389b7c`  
		Last Modified: Wed, 21 Jan 2026 19:01:31 GMT  
		Size: 583.0 KB (583040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2671d786d3974d089d22b6cb48fe7f66e1e8908e2d74d238a46c5b2e1b32ee9c`  
		Last Modified: Wed, 21 Jan 2026 19:52:03 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a85f84d03272750011d9471822bf5c0deea3499b5fef3f5bfc4c9710349642ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163811456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac341da44732b71b0509f4c5de9c88533bf505a551f6984fdca0a8f81d08955`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:33 GMT
ARG version=21.0.10.7.1
# Wed, 21 Jan 2026 19:01:33 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:33 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed197f84715ef0ef979d302a0da27da3341c03c36879e415591cea9dc0bdf176`  
		Last Modified: Wed, 21 Jan 2026 19:18:25 GMT  
		Size: 159.6 MB (159615717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1844a636381ded15ac5ede7225ce461462ba16d423538b621a7c96a285699c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.7 KB (592690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fe4883d3656f3f8646eca7f99156d0652ef17fe1d2f016e4c5a4b83c7cc5ad`

```dockerfile
```

-	Layers:
	-	`sha256:f4f9d4bd6510ccb2b548fc72a08ed71505a550d2fe690bef9a820fa39700a91f`  
		Last Modified: Wed, 21 Jan 2026 19:52:08 GMT  
		Size: 581.9 KB (581857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8027d695ae6d4d14f0603d2221ee7922e5812d2f31dbd8a3e7e3f6d65999d2a`  
		Last Modified: Wed, 21 Jan 2026 19:52:09 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json
