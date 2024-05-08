## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:d801a9cb39c58bd783848058affb9eaa64c7c08e6db239a79377d6be098b0e42
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

### `caddy:builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:a7d8da631168333353b5e4899f22b362669fbbc9c5aa009bf2c61864182c5e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77068124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b48021f4bf398e8b4dbdc809436a8665c9fb90091d96f90af5e2aaff7ac5447`
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
	-	`sha256:7862e08f4a3ed79ba32d02613b9c596dea827892605f23ebad6c4860ecfd1a4d`  
		Last Modified: Sat, 16 Mar 2024 08:03:57 GMT  
		Size: 284.7 KB (284695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f24391b3a8e63b07188d999f38818512667dd56c786cadf6ba3b0ac0150c55`  
		Last Modified: Tue, 07 May 2024 17:32:25 GMT  
		Size: 67.0 MB (67007954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c1cc01a5857be6537ca732ae0ffb65298345b87fbfc6ea8b3d0325be36c3eb`  
		Last Modified: Tue, 07 May 2024 17:32:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb4dd08042db792c135d7bcc8c052210c713da6b115d7ce24f947f562b7cfca`  
		Last Modified: Wed, 08 May 2024 16:51:33 GMT  
		Size: 5.0 MB (4972808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f2e7caa1e36832501afc97a4b0662d8663cf14d9622b87a320258dde0d0314`  
		Last Modified: Wed, 08 May 2024 16:51:33 GMT  
		Size: 1.4 MB (1399485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d01228ea43a02f83937496db036c88f1a6c0828344402f2ef44e684c77c442b`  
		Last Modified: Wed, 08 May 2024 16:51:33 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:d8154e9abc2e980093555d86036f86460ed05d78d36c97f39b9518e8a8048d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 KB (283394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc3f762a554e262c6418e3ca38af334649a883d6d76b51ca9724fafe576b997`

```dockerfile
```

-	Layers:
	-	`sha256:f0b96fc3ac8d8a6beecc8ef14212b60481b5bdb89fe0cb210e1ad0e1b21a2641`  
		Last Modified: Wed, 08 May 2024 16:51:33 GMT  
		Size: 263.1 KB (263050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ac7752eadfd7a2b525b06451388a1801eac0adee62074cb6c125f3b137eafdd`  
		Last Modified: Wed, 08 May 2024 16:51:33 GMT  
		Size: 20.3 KB (20344 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:7ae59b7e56fa733ba362f2335b301254b58b32cb8edb54cca1ee9be83cf8ee64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75479663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1eed464ec724b2655be80affd87a2ce37f8606e4e554633f706e919f6a6d706`
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
	-	`sha256:18595ac3d5791e4d7e7dbcffcbf63e97e29974bd7191f7779889293f06709605`  
		Last Modified: Sat, 16 Mar 2024 01:27:12 GMT  
		Size: 284.9 KB (284879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8221f6a4cffcf6f1e5edb9bd00c61b2a5c6ae12a7ddbe95b65f74f1f7b48c469`  
		Last Modified: Tue, 07 May 2024 17:53:46 GMT  
		Size: 65.8 MB (65766903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbc6120bd8c54608b8840b943a5f2680574bd18cfd001123c8d2769004ba56c`  
		Last Modified: Tue, 07 May 2024 17:53:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5385953b4f553b8571620a8a0298ee29ed556f368b8e80461e4c6b6ae93e69b`  
		Last Modified: Wed, 08 May 2024 16:56:41 GMT  
		Size: 5.0 MB (4958565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb4b8fcb978d13c183de77b86ee70ab52fb1805b38ddf2cfbd01a5b4b42efb9`  
		Last Modified: Wed, 08 May 2024 16:56:41 GMT  
		Size: 1.3 MB (1321616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b2ef53a28dc79a17b93409620c736b2f42c59e59cf18d13c3f846af6e1e535`  
		Last Modified: Wed, 08 May 2024 16:56:41 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:8ca69f22d9bd67b095eb152ff0a5c0db75291b93d38928be426f35da7f0e7b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c9fb834230601cf3a781db3a9dbef3d55ef6db1aa1f60996da0cd20fb0bcf1`

```dockerfile
```

-	Layers:
	-	`sha256:d3f1e6e26d91986ed20921cdc6db2855f52a6e506033264f9f6c7835b488f28f`  
		Last Modified: Wed, 08 May 2024 16:56:40 GMT  
		Size: 20.2 KB (20240 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:57e9033ed99bde1b04b1ad0e92fc7a56aef3c8698167fc669e29f820ee97955e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74785756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28e94baefa246661a5deac3a9bcff7a17a17c8405fc637322a9fb091c8ce911`
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
	-	`sha256:03de95814623b83a4328b4db2e23b14214f57c18389a27379988469d9b6bbccc`  
		Last Modified: Sat, 16 Mar 2024 00:51:49 GMT  
		Size: 284.1 KB (284082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae3b2324373ed49089c6fae60d6c941aa4b8960fc402e4f665f66d9699b9856`  
		Last Modified: Tue, 07 May 2024 18:32:23 GMT  
		Size: 65.8 MB (65766943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8cb2c3f5b006bc6dbbb56c56d008271bfa1092095e701bc0278a3a6dbc8291`  
		Last Modified: Tue, 07 May 2024 18:32:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb67b1fe5cb800d0f10a06e26edab938f80283f0e89b06f4a9221f1caa38141`  
		Last Modified: Tue, 07 May 2024 20:04:23 GMT  
		Size: 4.5 MB (4514432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979ad0dab28b40feed8c39fab770a7e526e0335c61f6191e556ee0cf647c7b41`  
		Last Modified: Wed, 08 May 2024 17:24:10 GMT  
		Size: 1.3 MB (1318264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7122a0b6c285dbdfe59774d2de9bf60ba4edaed6e4b26d372e1afb2edec18d4`  
		Last Modified: Wed, 08 May 2024 17:24:10 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:fdca3672e60957b54815e8ed2469485da42bfd977bf855453a6f6f587b4af29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 KB (285312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c79055e372ea478f4fcfa641fd574c601a5604a321ab11ea345fe760546444e`

```dockerfile
```

-	Layers:
	-	`sha256:81f3194a7a7a40cabd5d4c06c7f99667e8a457024a74ac0ad802c67d022dac2c`  
		Last Modified: Wed, 08 May 2024 17:24:10 GMT  
		Size: 265.7 KB (265666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7273cef9a0c47b0f4ea4a35f5401dea7a9f84f0d00fcedefe4f3041832f5bf97`  
		Last Modified: Wed, 08 May 2024 17:24:10 GMT  
		Size: 19.6 KB (19646 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:304d65fa80a604d16734f10f7b24cb5fe411e2544902073681e3b77a964a57b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74089208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c1c7ee20762a65dff2197ead8c8d5393fdaa1edfc57fdbddbef13593f13898`
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
	-	`sha256:a69c4102457739613c6fcb205a5a8e7dbc8383d57dade0a4502b1bca7b100a4d`  
		Last Modified: Sat, 16 Mar 2024 02:38:03 GMT  
		Size: 286.3 KB (286314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081870b0a3a575371a47514a1587d72b3ed20393e0b814e018af644ae02d4354`  
		Last Modified: Tue, 07 May 2024 17:44:29 GMT  
		Size: 64.1 MB (64106740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5342516f2484c34a836a7a863eb81f3105c46c1073d5369d8d555cd3886bf21`  
		Last Modified: Tue, 07 May 2024 17:44:21 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bba47559bb65192116ff634bc5d776d7e73d55d8ba3412a36c9b1c5d3a69cf`  
		Last Modified: Tue, 07 May 2024 19:22:11 GMT  
		Size: 5.1 MB (5063862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bcd29e26ec8031e395a727e3070ee0e25bc834f8111c18581618663f06ea58`  
		Last Modified: Wed, 08 May 2024 17:17:09 GMT  
		Size: 1.3 MB (1298288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc1a630d1ff6c946122bf9031b5ab2bca9106fb7f496df07006c352720c0a9c`  
		Last Modified: Wed, 08 May 2024 17:17:09 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:730e3e52adb968ed39685f1b5b01c1203b0e62ff14b086a843cd6ffcd42c5493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 KB (282618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65657bb86a7314292f33fa4f330256eb9f29fcc6607ebb8916e8b232448ed41`

```dockerfile
```

-	Layers:
	-	`sha256:7674770c0e57e813eeedb157c9f0953bb54319da094eaf5dfc03fb40385cb0ad`  
		Last Modified: Wed, 08 May 2024 17:17:09 GMT  
		Size: 263.1 KB (263069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62f807ccd32a146dea536208b30334c566aeceadff916cc61c1ca692ddbd04a2`  
		Last Modified: Wed, 08 May 2024 17:17:09 GMT  
		Size: 19.5 KB (19549 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:220a2625ea1da79eb140b2743a20ffe3530acb58a2f031048b56366cf6e43a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74329720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727a70954bd254964740e4ec92a7d631440156a9b69b40e778988c51839bef3e`
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
	-	`sha256:e315e4c0ee7596e0eb7cc17d622c433e9fc4ef254b722e11e6794265328ea583`  
		Last Modified: Sat, 16 Mar 2024 00:32:12 GMT  
		Size: 286.7 KB (286670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fc9e25661d2224b1534ceb0ba5c9ff0c5016f5d59e9816759f3729a4e18b0`  
		Last Modified: Tue, 07 May 2024 18:29:57 GMT  
		Size: 64.1 MB (64129233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e19e7bd306dd0de5211dc8475a54d787e86a0a2dfef2613727484209d478b7`  
		Last Modified: Tue, 07 May 2024 18:29:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76c4fac121b4f5d1b8841ec5dc1bdb096024b0342e08b35bee31b211513f31b`  
		Last Modified: Tue, 07 May 2024 20:06:06 GMT  
		Size: 5.3 MB (5270885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9995c539786b4135b94728ba98567e3ae4b9ed61593820990bdfd60af2968546`  
		Last Modified: Wed, 08 May 2024 17:18:14 GMT  
		Size: 1.3 MB (1293802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159f07d7594bebf85ea0bd4157116e8ca003b5d22b986c591726ad3e8ad9a691`  
		Last Modified: Wed, 08 May 2024 17:18:13 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:6a1ddb3c111777660332f7feb04b9c04af26cd415f42e3e0ca4ac846204922da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 KB (280783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fceb44c6cab6bf83212c26cef4bfda90dc98b74d2ecc8a01a69575dbbdc4ee2`

```dockerfile
```

-	Layers:
	-	`sha256:4c27cf55c40fd7e264ba4a8c71d04fc659ef75fb589114a330669ec95794a31b`  
		Last Modified: Wed, 08 May 2024 17:18:13 GMT  
		Size: 261.2 KB (261188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5e4ce1aeeee3f1b4b4ca9f526722ba49468920cf0c189b80176c735c7514d9d`  
		Last Modified: Wed, 08 May 2024 17:18:13 GMT  
		Size: 19.6 KB (19595 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:08770bf49f5ce99ea2927c50616322512318092d78b70f0f6ed8c8d45b1c817f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76194057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7ff8a6d39c9616961784e6a83e133aeba79927a055e409ba81c9adf65eb90a`
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
	-	`sha256:3e1b6899ff00172fd5c809d57028913a3c5aead2c05d0c3c01b15a5249c4ddec`  
		Last Modified: Sat, 27 Jan 2024 05:46:31 GMT  
		Size: 285.1 KB (285091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8e0687b504482015ac9005e22ec13bef257c78cb214d60d9dee8e515773f61`  
		Last Modified: Tue, 07 May 2024 17:54:02 GMT  
		Size: 66.2 MB (66221362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc3db35ea30291b063271e70e924d7f5da620868405686352475408ac19ecde`  
		Last Modified: Tue, 07 May 2024 17:53:51 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5108c9208de45aa3a777fa6c18a351382907af694959c3cbd3a8707ad61771fa`  
		Last Modified: Tue, 07 May 2024 19:06:20 GMT  
		Size: 5.1 MB (5117163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec9e0777be6449feb3ec64626f66582dc620bb6572dce8f196b0c9fb232bbeb`  
		Last Modified: Wed, 08 May 2024 17:18:03 GMT  
		Size: 1.4 MB (1352270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f2ef7bc0c54f39182f74a0353cef348b6344a14045fbf21395d36b75fe19b3`  
		Last Modified: Wed, 08 May 2024 17:18:03 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:52a6fc37a5d4bb8a1f43acb586e9fbbb9272054103f1355a45468610fefff222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 KB (280623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a7ce7747c8162b27e053bb1b117b4bf5d623ae56d34edb5a22c25c4578d852`

```dockerfile
```

-	Layers:
	-	`sha256:e1e3a691ed8616346ea47aa2b189288505a715af6479c9dadb47f4e22ce55922`  
		Last Modified: Wed, 08 May 2024 17:18:03 GMT  
		Size: 261.1 KB (261094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f21d8139ec9ae3d0f1b9156a3fb3d814a18134daea7f578b720f21e567da9f9`  
		Last Modified: Wed, 08 May 2024 17:18:03 GMT  
		Size: 19.5 KB (19529 bytes)  
		MIME: application/vnd.in-toto+json
