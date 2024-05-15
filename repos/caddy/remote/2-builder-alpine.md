## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:1bd8cac07af2bd33d70ca237e3fa5324af77ff08d2868e890ef971eb2c9222b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:2d0f98ee37151fac228829512d71cd60683bcca714b42a2accfd5b2ed0eef309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77076844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da2caebf0c82328df2582d2154aea90549512f5f8075a1d211888861edc36d0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ea3408117e6ad5da2610d98c7aaaa6ab17d9280a7f00e54b78f4a8af1a13e6`  
		Last Modified: Tue, 14 May 2024 22:57:18 GMT  
		Size: 293.4 KB (293394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91320369b822ebdafa53385de29218150ed2e0c9432c803ae9ab0917b1c13e05`  
		Last Modified: Tue, 14 May 2024 22:57:19 GMT  
		Size: 67.0 MB (67007431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0406650e82959e8bef670a6825ebc6caab141ed9ad0670923af9d5998de85b1b`  
		Last Modified: Tue, 14 May 2024 22:57:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd54b29b355af23f51f47454c3e17573db8b78d7b52ce85f0455a2e39d7fa074`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 5.0 MB (4973399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbee18c299cb69dbccc6437fb935315abe5ea1a53244f52a8ef81bf71b3ec7c`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 1.4 MB (1399486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3962e3b1e39ca0549762f19fbf5ce97673a3c8e25e572443e99130f629becf`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:6f76e9858ca4547fe58ff97bd2ffc98029feb869b1dfc98633fd6f628b314292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 KB (288373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d01d8efed7000405f724e82795e9cc915343e431cc02e71f7cb5c25dc349bc`

```dockerfile
```

-	Layers:
	-	`sha256:746b0306cd3cb1912a3fc855ffc1003e09c16f75c165c8632bfe6eb00f877847`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 268.0 KB (268019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8416aff5ff51dc4e8fe28c6decdd0e3d91752160f7da7909a202850f8bd690`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 20.4 KB (20354 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ac7c2575373554f84061a11c48e068678edf889b364d17fc18cae4e80ce71e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75488808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48147857ead25ab7ee7a77aa74a59e293fa9eca878fe8afdd536d5f143675028`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27c253e1ccd740370512ac16dc1198d4cc7e5f79502d830e914be781d2a53ef`  
		Last Modified: Tue, 14 May 2024 23:02:34 GMT  
		Size: 294.1 KB (294052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2d6f1f07c341f159f464047d7dfc24c2fe15b8492e49ca6864e4bb242a3ec8`  
		Last Modified: Tue, 14 May 2024 23:03:32 GMT  
		Size: 65.8 MB (65766197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ab3f344a28c5c3a77d5b42ed139c704c1a62bb86a51a6d424570cbeddca4f3`  
		Last Modified: Tue, 14 May 2024 23:04:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b167340b71c005d807677fbbfbac662cedcb4fec7ccda3d644fa2d7cd2160000`  
		Last Modified: Tue, 14 May 2024 23:59:49 GMT  
		Size: 5.0 MB (4959292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db00701b53c1d5eee7ae5f0370ad0e2bf8c7624155e1ccd2197c482e47a9b928`  
		Last Modified: Tue, 14 May 2024 23:59:48 GMT  
		Size: 1.3 MB (1321618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3610115cc7dedfcb5e2e244108591d41fbe0430d9c192503193a6f2a0e0c62`  
		Last Modified: Tue, 14 May 2024 23:59:48 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:65e3693b278d4ef7c1c71f462d35e072feb067d47d882a6357051558d5f46278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 KB (20292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883db6588355f9fff45c61143a3c184d6b5360f70087363d292d63c4ffd73363`

```dockerfile
```

-	Layers:
	-	`sha256:f9d8b3568f220dfd1bdb1ddf4e41df2a13ced2a403b7245c9a18e0b60d52fd7b`  
		Last Modified: Tue, 14 May 2024 23:59:48 GMT  
		Size: 20.3 KB (20292 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:09a6c1b0e1bd5044d5c064715c0aa03b90e6940ba650cf16faef929b3f79fa04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74794769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a0acea946d5a81787cb9fe18c7071c5aa68a591344d13571c0ce51a5e470d1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1e32b4becad7a3ff9750dab0a6195a4136fe3417839cd5d6ced26f77c37d79`  
		Last Modified: Wed, 15 May 2024 08:39:33 GMT  
		Size: 293.0 KB (292954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab304151744566becd5140e866f02946274de2d4d2a228bdba72a0e4dddfa248`  
		Last Modified: Wed, 15 May 2024 08:40:52 GMT  
		Size: 65.8 MB (65766163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ceb4452378bf5d66c4470fe48fe8427a79ec5fdc8ddb8ea1c7fc02a13ce65b`  
		Last Modified: Wed, 15 May 2024 08:43:33 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3270f12d361d5c63e9937439d8ff8f1080a9e9af98e31682da7f8d67a613c759`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 4.5 MB (4515403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058f91ac0045b9c67e0b445141195571ad95b6f59a25eb681889ad831b1498dd`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 1.3 MB (1318268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4d6b7782ec5dfb52798f8e6b9b9ab819fa68f6eb20afac4a297ba01be2efae`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:7642ba203742b9113008f284cfdf3548460cbae2ee69ecb2454eb8c735b96da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 KB (291146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94a8f15a57f45b959c2c2fc76cdd718d5ad776676b941690a80ec419f5487c6`

```dockerfile
```

-	Layers:
	-	`sha256:d711709c34958acee3c07ef7e1919d12e4928a2ca18487dd1819cbe2b91d6ae5`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 270.6 KB (270635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41bcb88e50c5a338a29305fce33e34c339529ad379da7ba7d1cd2088bf08e935`  
		Last Modified: Wed, 15 May 2024 09:20:10 GMT  
		Size: 20.5 KB (20511 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:022c416ba80bd913b0d16582f1065f5c4b8ad34f219855b8a021c94d106524c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74098271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d00e35d265158288ca2a81ad2fdfbedc5b7035f13ab9cd1b998d4991d8fa37`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84613e011ca8867fd82ad1a4602a9c5ca1629a8c52b91548ba0a8ce39bc63bd6`  
		Last Modified: Wed, 15 May 2024 10:25:13 GMT  
		Size: 295.8 KB (295843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a7eb7dd16a3cb705d643f2c1b3ccb0cce9120eef39b1b1844864195af6c32`  
		Last Modified: Wed, 15 May 2024 10:28:17 GMT  
		Size: 64.1 MB (64106287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788e89ea89d463b8bcafc4d5b552bddaa08b72930505c3e5b6917da512bca47c`  
		Last Modified: Wed, 15 May 2024 10:29:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5119b2251effb8f032617ef72426ede6300a48b24df3322f8180c5112fcb1488`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 5.1 MB (5063898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab86c9ac1c04673c91199de9df55b222aeb76d630df93b84c38cabab987ca9b`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 1.3 MB (1298290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e12372ead2b5522c0b9d32638dcec3d9780a4b4495fe0327787759f670419`  
		Last Modified: Wed, 15 May 2024 17:32:45 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e620ba0bef62789334c010b7cacf7a13de0927228fc5d74634b118f93d8a5ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 KB (288452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988be65311a6efef34a6bdac2f8dcba490cc5ae7a90c13a7b4b72cd68956fd79`

```dockerfile
```

-	Layers:
	-	`sha256:b860d1f348c1e8c34388faf32ca1f31601f367503a56b8482f22e27d112f725c`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 268.0 KB (268038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0144585ac3a8859d627186fb46c2dc5e2e025006a8801d6718aca937f207427`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 20.4 KB (20414 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:ed5114faaef7109c9b6d09463fe6cd92b3012e1b89d7d4881ba567e2215f37c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74339423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa437d1d5649dee8d678ada0475d1bf336545ad8ffa4a692c19bba4fe496c25f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b2216e014970a83beea11c197a24ccf7f0027acc0d35a08b3a3b2c976b5eff`  
		Last Modified: Wed, 15 May 2024 04:47:32 GMT  
		Size: 296.3 KB (296270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b672324861585f05676c004287c9eeb3ec624b063c08e6689139af3a2f1ed3df`  
		Last Modified: Wed, 15 May 2024 05:01:36 GMT  
		Size: 64.1 MB (64129414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4969b1c1838dc52cc8a18a048524a037b980febaecd9563210c4df1a96604b42`  
		Last Modified: Wed, 15 May 2024 05:23:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abcaf0a32c421ab0105f8a6eb25fa2862e92a57fe5c68c0de96702a1496789d`  
		Last Modified: Wed, 15 May 2024 06:09:04 GMT  
		Size: 5.3 MB (5270859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14972492f5cb274941b32172d5bccee08aba0eb45858ff97fe6fb9f45719fed`  
		Last Modified: Wed, 15 May 2024 06:09:04 GMT  
		Size: 1.3 MB (1293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad16cdba266ead2ca15865cafeddfa415df7136a8ea60d18e820ce12c1407b61`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:2b40a03abefdfce61a9c05a652fbccf303ce8b02a57d74d4a4e0b3faebc448e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7793b7cdf8a3c9fe0b5515824960473b044a9be5b121a8763e7f63d45e27617e`

```dockerfile
```

-	Layers:
	-	`sha256:a992b851d066d8fb1da7d613d1d07540e1edd799d4b99a7da6d8c73629f8982c`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 266.2 KB (266157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b35b875bfd977ef42a74ac4b84ec1b6d05e4daea22d2a52db56fab59e5a6663`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 20.5 KB (20460 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:a47a2a03f9a9b7816a7a1113d57cd13a6291da16c23508710b0ca70debbb86d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76203648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e88c1f13b847682609243dade2de8bb68fc2643f3ef6c50cf558e301e6f05f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1a1d4bba7fb363f0ef2f025a4c6c441c7026445c4b9c955c509893576ea917`  
		Last Modified: Wed, 15 May 2024 02:47:56 GMT  
		Size: 293.9 KB (293929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109cf0320d2fb40b9f56e4b0b8249d43214d262e3aaa145e939c8d7354258d89`  
		Last Modified: Wed, 15 May 2024 02:49:19 GMT  
		Size: 66.2 MB (66221838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f36caa761931318dec5fb4c6712ab1ab66f9992473dd4c5bd890ad223c3ddd`  
		Last Modified: Wed, 15 May 2024 03:08:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c238da3c7fff1913d7b837e4c0413d72ec94e770a03bf0abcdd03ee7f233c6`  
		Last Modified: Wed, 15 May 2024 04:14:20 GMT  
		Size: 5.1 MB (5117490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4576d2e047b1a8655a7d7395721fa5506df982c1b78ffc068954ec28445a9b7`  
		Last Modified: Wed, 15 May 2024 04:14:20 GMT  
		Size: 1.4 MB (1352270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56b016932ac8f843faffdd88108c80fcd9b38b5ac893706dc6780d4777eb88d`  
		Last Modified: Wed, 15 May 2024 04:14:20 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:51196241f4bb937ea188f006f7ce0120d183680a55447da6b30b27c68f3d44d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 KB (286453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03069f12e51484e13fcfe4b6c7d03806f5efafe115a28c761003f672133cde4e`

```dockerfile
```

-	Layers:
	-	`sha256:074231774abc16fdbd7854582de2bfed128864d0fdabc7f75ee0b1cb2c153ebb`  
		Last Modified: Wed, 15 May 2024 04:14:19 GMT  
		Size: 266.1 KB (266063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77307ab5bd56ac3f136ed6992239aa495abc11b377b0e06d0fc98228b8c830bb`  
		Last Modified: Wed, 15 May 2024 04:14:19 GMT  
		Size: 20.4 KB (20390 bytes)  
		MIME: application/vnd.in-toto+json
