## `caddy:2-builder`

```console
$ docker pull caddy@sha256:11d1adf0651b0e447069bebb6c7276e49cc8677a24f67a0eecd72710ddc6fd37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:4588afebc1380ee42886ac7013cca31b72df39e540925caff3c89960814a91c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77068125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b55dc9a15cff27099d55b6919a44a4de51991cfebdfc1137e052a192396146e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:02:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 01 May 2024 14:02:44 GMT
ENV GOLANG_VERSION=1.21.10
# Wed, 01 May 2024 14:02:44 GMT
ENV GOTOOLCHAIN=local
# Wed, 01 May 2024 14:02:44 GMT
ENV GOPATH=/go
# Wed, 01 May 2024 14:02:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 May 2024 14:02:44 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 01 May 2024 14:02:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 01 May 2024 14:02:44 GMT
WORKDIR /go
# Wed, 01 May 2024 14:02:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_VERSION=v0.4.0
# Wed, 01 May 2024 14:02:44 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_SETCAP=1
# Wed, 01 May 2024 14:02:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='bd3f08b2fe678b877a3ba23c8801749c513f066f8c2f8fdcfb74cb0cf305a0063e268f44c407eb614b6157d09357913428462153d16b969a2828c1998872b994' ;; 		armhf)   binArch='armv6'; checksum='5011a139379d5d62d5c3bb18037919667e8c9bf98fec1d3e4f5ab6ebe82f43e51d64fdbce1d673085b27a9dd23f41a1991141caf9aedd28ef5956b8147320144' ;; 		armv7)   binArch='armv7'; checksum='06f5ee41eda0571c855d4fcef6f523f892e37b560815f3f5014fe985090173c79d4abbde0efc80d4491d6ac3cfa5609eb220d81a49fb3307b08283c107b81412' ;; 		aarch64) binArch='arm64'; checksum='b730a207efed951846ee322755c16042cc8135a4b3ae10bb550e3801306b3811b75a72f4dfbfdb2bbe38d4247ce30d52051ca85277abafeb50616f6387e6cb58' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='139a13652eb5f16a84cc6dd3255c6822306487cd3414a76fc174fc2d96bde08701abacdbc7ece282e64409876eb946b1665909bb53413cd1b0574ce1eb1eb897' ;; 		s390x)   binArch='s390x'; checksum='a722acbdbf74727e3b8fa14a1e7638b2dbe0e0aeb32c8d5af98fd274cd22bb5ea756072a6f3a46bfc8345503deddb876105cb0f5f935e30fd1525962914ed5c1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.0/xcaddy_0.4.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 01 May 2024 14:02:44 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 01 May 2024 14:02:44 GMT
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
	-	`sha256:dace60945dd1e3faf1feb4fe3dd6a3ca8273cc800d5895c904db88b0a2641efc`  
		Last Modified: Tue, 07 May 2024 18:51:38 GMT  
		Size: 5.0 MB (4972834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98698fd20f14b16fc984d25e142724da47361dc14bb91bc2d5535275756d159e`  
		Last Modified: Tue, 07 May 2024 18:51:38 GMT  
		Size: 1.4 MB (1399460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d8fd09f603208f972aaeac055118689390f4b41c86ed2db6557e4d62bdef0a`  
		Last Modified: Tue, 07 May 2024 18:51:38 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:9768346bea176db7e95f084a5555d5cbe7953fd429f8b19c34520eec585161e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 KB (283394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59958b7393fa1fa383ce1eec1893dcd60366c3e2f46861b93b0b3e83151ff988`

```dockerfile
```

-	Layers:
	-	`sha256:0da6c52cc997e9239e8d0667ccbdfe0e7deb055e9ef4c840cc47a489aac8fa29`  
		Last Modified: Tue, 07 May 2024 18:51:37 GMT  
		Size: 263.1 KB (263050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d7457503964867fae72ce94f28d99a11a6c3d6be14232feb224f68d4363137e`  
		Last Modified: Tue, 07 May 2024 18:51:38 GMT  
		Size: 20.3 KB (20344 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:cd0554254a69c1fe9fc0dc87da6b2b6eff6b2752f399f07fe27b14acdebf0178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75479487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e679674ac2d956dfb4acc809645258033d14fc647578e333011b19ce65b902a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:02:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 01 May 2024 14:02:44 GMT
ENV GOLANG_VERSION=1.21.10
# Wed, 01 May 2024 14:02:44 GMT
ENV GOTOOLCHAIN=local
# Wed, 01 May 2024 14:02:44 GMT
ENV GOPATH=/go
# Wed, 01 May 2024 14:02:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 May 2024 14:02:44 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 01 May 2024 14:02:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 01 May 2024 14:02:44 GMT
WORKDIR /go
# Wed, 01 May 2024 14:02:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_VERSION=v0.4.0
# Wed, 01 May 2024 14:02:44 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_SETCAP=1
# Wed, 01 May 2024 14:02:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='bd3f08b2fe678b877a3ba23c8801749c513f066f8c2f8fdcfb74cb0cf305a0063e268f44c407eb614b6157d09357913428462153d16b969a2828c1998872b994' ;; 		armhf)   binArch='armv6'; checksum='5011a139379d5d62d5c3bb18037919667e8c9bf98fec1d3e4f5ab6ebe82f43e51d64fdbce1d673085b27a9dd23f41a1991141caf9aedd28ef5956b8147320144' ;; 		armv7)   binArch='armv7'; checksum='06f5ee41eda0571c855d4fcef6f523f892e37b560815f3f5014fe985090173c79d4abbde0efc80d4491d6ac3cfa5609eb220d81a49fb3307b08283c107b81412' ;; 		aarch64) binArch='arm64'; checksum='b730a207efed951846ee322755c16042cc8135a4b3ae10bb550e3801306b3811b75a72f4dfbfdb2bbe38d4247ce30d52051ca85277abafeb50616f6387e6cb58' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='139a13652eb5f16a84cc6dd3255c6822306487cd3414a76fc174fc2d96bde08701abacdbc7ece282e64409876eb946b1665909bb53413cd1b0574ce1eb1eb897' ;; 		s390x)   binArch='s390x'; checksum='a722acbdbf74727e3b8fa14a1e7638b2dbe0e0aeb32c8d5af98fd274cd22bb5ea756072a6f3a46bfc8345503deddb876105cb0f5f935e30fd1525962914ed5c1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.0/xcaddy_0.4.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 01 May 2024 14:02:44 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 01 May 2024 14:02:44 GMT
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
	-	`sha256:cb43ce50c4f6408650f31a378fb0ebc582982950b2cd362ecac340c6b78ede54`  
		Last Modified: Tue, 07 May 2024 18:54:05 GMT  
		Size: 5.0 MB (4958581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201cf5c1de96f961427663e275f0ff60f98b4df275645eef80cd8c6ed5947ac7`  
		Last Modified: Tue, 07 May 2024 18:54:04 GMT  
		Size: 1.3 MB (1321424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7841627e496b08e64fef18130b36ab03d4c7575d32f791330d0e903af3058ef`  
		Last Modified: Tue, 07 May 2024 18:54:05 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ea06ab11351e4005de31b8315a4b8ea48fba0654e0840b6e5ed193f360e5ca35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f06ce0b23e7c2c0495baf9a02a3135a64173393f9c0dfcc7d49188e52062a9a`

```dockerfile
```

-	Layers:
	-	`sha256:6b22de10c44fcb0b1e0830502120360f24ca4499aabd010dcad703f4dce82a06`  
		Last Modified: Tue, 07 May 2024 18:54:04 GMT  
		Size: 20.2 KB (20240 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:f70fbec00d4bc151a0ebab03e3767318fe8b2036027e59870362c462fc0c2d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74785585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dce0e9bee0cf1d032d650e8590a4f58c51ce2ab4a8858e847b058908ce89db`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:02:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 01 May 2024 14:02:44 GMT
ENV GOLANG_VERSION=1.21.10
# Wed, 01 May 2024 14:02:44 GMT
ENV GOTOOLCHAIN=local
# Wed, 01 May 2024 14:02:44 GMT
ENV GOPATH=/go
# Wed, 01 May 2024 14:02:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 May 2024 14:02:44 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 01 May 2024 14:02:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 01 May 2024 14:02:44 GMT
WORKDIR /go
# Wed, 01 May 2024 14:02:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_VERSION=v0.4.0
# Wed, 01 May 2024 14:02:44 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_SETCAP=1
# Wed, 01 May 2024 14:02:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='bd3f08b2fe678b877a3ba23c8801749c513f066f8c2f8fdcfb74cb0cf305a0063e268f44c407eb614b6157d09357913428462153d16b969a2828c1998872b994' ;; 		armhf)   binArch='armv6'; checksum='5011a139379d5d62d5c3bb18037919667e8c9bf98fec1d3e4f5ab6ebe82f43e51d64fdbce1d673085b27a9dd23f41a1991141caf9aedd28ef5956b8147320144' ;; 		armv7)   binArch='armv7'; checksum='06f5ee41eda0571c855d4fcef6f523f892e37b560815f3f5014fe985090173c79d4abbde0efc80d4491d6ac3cfa5609eb220d81a49fb3307b08283c107b81412' ;; 		aarch64) binArch='arm64'; checksum='b730a207efed951846ee322755c16042cc8135a4b3ae10bb550e3801306b3811b75a72f4dfbfdb2bbe38d4247ce30d52051ca85277abafeb50616f6387e6cb58' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='139a13652eb5f16a84cc6dd3255c6822306487cd3414a76fc174fc2d96bde08701abacdbc7ece282e64409876eb946b1665909bb53413cd1b0574ce1eb1eb897' ;; 		s390x)   binArch='s390x'; checksum='a722acbdbf74727e3b8fa14a1e7638b2dbe0e0aeb32c8d5af98fd274cd22bb5ea756072a6f3a46bfc8345503deddb876105cb0f5f935e30fd1525962914ed5c1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.0/xcaddy_0.4.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 01 May 2024 14:02:44 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 01 May 2024 14:02:44 GMT
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
	-	`sha256:9d920b8491f17f82f62225b4838b6502a93911d5b6e0579630b6f043fff95e71`  
		Last Modified: Tue, 07 May 2024 20:04:23 GMT  
		Size: 1.3 MB (1318097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fe645e08ade99b17f58c1007827415ae86654cbd30359e8a31a2c99ae215f5`  
		Last Modified: Tue, 07 May 2024 20:04:24 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:75fe8519337ef1e4b69176a7052ded9b7e31e66e22a6dbd39c7a6d57603ca68d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 KB (286125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce56b2eb7eb69979030f665cbf0d4194487ec2dc13c9c97bc830ee74d8461ae5`

```dockerfile
```

-	Layers:
	-	`sha256:9d6a4a380d8b3af30458b50d30d8dc536b4197d3150cbf457ba519cd95d1774d`  
		Last Modified: Tue, 07 May 2024 20:04:23 GMT  
		Size: 265.7 KB (265666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e533342445ae27787e04dfa6a09f2f4cfea40c80f6262b31733fb655992154e`  
		Last Modified: Tue, 07 May 2024 20:04:23 GMT  
		Size: 20.5 KB (20459 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:47aa572930b27906e0740a6453192891e465440c7489005ecda841ce75f99674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74088987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44abb60d64b93e7d4b6e5376fb213542adef7b601397315b5c72bcdf8debe04`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:02:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 01 May 2024 14:02:44 GMT
ENV GOLANG_VERSION=1.21.10
# Wed, 01 May 2024 14:02:44 GMT
ENV GOTOOLCHAIN=local
# Wed, 01 May 2024 14:02:44 GMT
ENV GOPATH=/go
# Wed, 01 May 2024 14:02:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 May 2024 14:02:44 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 01 May 2024 14:02:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 01 May 2024 14:02:44 GMT
WORKDIR /go
# Wed, 01 May 2024 14:02:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_VERSION=v0.4.0
# Wed, 01 May 2024 14:02:44 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_SETCAP=1
# Wed, 01 May 2024 14:02:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='bd3f08b2fe678b877a3ba23c8801749c513f066f8c2f8fdcfb74cb0cf305a0063e268f44c407eb614b6157d09357913428462153d16b969a2828c1998872b994' ;; 		armhf)   binArch='armv6'; checksum='5011a139379d5d62d5c3bb18037919667e8c9bf98fec1d3e4f5ab6ebe82f43e51d64fdbce1d673085b27a9dd23f41a1991141caf9aedd28ef5956b8147320144' ;; 		armv7)   binArch='armv7'; checksum='06f5ee41eda0571c855d4fcef6f523f892e37b560815f3f5014fe985090173c79d4abbde0efc80d4491d6ac3cfa5609eb220d81a49fb3307b08283c107b81412' ;; 		aarch64) binArch='arm64'; checksum='b730a207efed951846ee322755c16042cc8135a4b3ae10bb550e3801306b3811b75a72f4dfbfdb2bbe38d4247ce30d52051ca85277abafeb50616f6387e6cb58' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='139a13652eb5f16a84cc6dd3255c6822306487cd3414a76fc174fc2d96bde08701abacdbc7ece282e64409876eb946b1665909bb53413cd1b0574ce1eb1eb897' ;; 		s390x)   binArch='s390x'; checksum='a722acbdbf74727e3b8fa14a1e7638b2dbe0e0aeb32c8d5af98fd274cd22bb5ea756072a6f3a46bfc8345503deddb876105cb0f5f935e30fd1525962914ed5c1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.0/xcaddy_0.4.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 01 May 2024 14:02:44 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 01 May 2024 14:02:44 GMT
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
	-	`sha256:3d9e6daa08f95f0cde90ae19e1914f66b78004439fa62d57a321ca919c3d10d8`  
		Last Modified: Tue, 07 May 2024 19:22:11 GMT  
		Size: 1.3 MB (1298071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fcf1d2c67273a2911bd7140e0dc1ce23e705f6c40ed81fe24917a8e8b7ccd7`  
		Last Modified: Tue, 07 May 2024 19:22:11 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:b184bd47e02b4ad2d9a84064cdb5ecaf8d6e9d10542fcc542435b88847d5dfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 KB (283431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df06fc2d373fba9b2666d3af54f808ff26b03cfff30ac4ea3e1e8c83e36dcbde`

```dockerfile
```

-	Layers:
	-	`sha256:d8b101abff9895c1b0c8dd2f8c17632eb4b292f7a0df75e84019d00a1a00dfc1`  
		Last Modified: Tue, 07 May 2024 19:22:10 GMT  
		Size: 263.1 KB (263069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93caf8206582dfdd153a75b2f9ccb1e9c700735bcffff3934e4dfef83d76e77c`  
		Last Modified: Tue, 07 May 2024 19:22:10 GMT  
		Size: 20.4 KB (20362 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:d74bd895597bc87d432200eaa34ed86959905cee0d9bb4422e490cf46b9e4202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74329530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871c7bd9cfe472feaca9d863cbac0ff593c487d5f4cbae109dced792c6d8e229`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:02:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 01 May 2024 14:02:44 GMT
ENV GOLANG_VERSION=1.21.10
# Wed, 01 May 2024 14:02:44 GMT
ENV GOTOOLCHAIN=local
# Wed, 01 May 2024 14:02:44 GMT
ENV GOPATH=/go
# Wed, 01 May 2024 14:02:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 May 2024 14:02:44 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 01 May 2024 14:02:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 01 May 2024 14:02:44 GMT
WORKDIR /go
# Wed, 01 May 2024 14:02:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_VERSION=v0.4.0
# Wed, 01 May 2024 14:02:44 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_SETCAP=1
# Wed, 01 May 2024 14:02:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='bd3f08b2fe678b877a3ba23c8801749c513f066f8c2f8fdcfb74cb0cf305a0063e268f44c407eb614b6157d09357913428462153d16b969a2828c1998872b994' ;; 		armhf)   binArch='armv6'; checksum='5011a139379d5d62d5c3bb18037919667e8c9bf98fec1d3e4f5ab6ebe82f43e51d64fdbce1d673085b27a9dd23f41a1991141caf9aedd28ef5956b8147320144' ;; 		armv7)   binArch='armv7'; checksum='06f5ee41eda0571c855d4fcef6f523f892e37b560815f3f5014fe985090173c79d4abbde0efc80d4491d6ac3cfa5609eb220d81a49fb3307b08283c107b81412' ;; 		aarch64) binArch='arm64'; checksum='b730a207efed951846ee322755c16042cc8135a4b3ae10bb550e3801306b3811b75a72f4dfbfdb2bbe38d4247ce30d52051ca85277abafeb50616f6387e6cb58' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='139a13652eb5f16a84cc6dd3255c6822306487cd3414a76fc174fc2d96bde08701abacdbc7ece282e64409876eb946b1665909bb53413cd1b0574ce1eb1eb897' ;; 		s390x)   binArch='s390x'; checksum='a722acbdbf74727e3b8fa14a1e7638b2dbe0e0aeb32c8d5af98fd274cd22bb5ea756072a6f3a46bfc8345503deddb876105cb0f5f935e30fd1525962914ed5c1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.0/xcaddy_0.4.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 01 May 2024 14:02:44 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 01 May 2024 14:02:44 GMT
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
	-	`sha256:35766dd97b2d6dead0d67674413e9c7b0e228f15f1015b467ff437100761c8de`  
		Last Modified: Tue, 07 May 2024 20:06:06 GMT  
		Size: 1.3 MB (1293614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf98aff7129ff0f9ebb47ebb7714a759c41693b22ef9104339b5a82d5e1a012`  
		Last Modified: Tue, 07 May 2024 20:06:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3a1f6deb46b2e12a6e3d548611b769a2976c581231028367801771eb18812df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 KB (281595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da116eb5cce97e280fc5949ed5db263a2437cbf08c9d2f291ea239d9f4d6356`

```dockerfile
```

-	Layers:
	-	`sha256:a92dbc7a1ea43e3b0415b4095e66b2715e71c7a9d84bff7f8540116eefb989fe`  
		Last Modified: Tue, 07 May 2024 20:06:06 GMT  
		Size: 261.2 KB (261188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6782f6dec5dd37fb2e551bda765a2d4e2f7bd11c0ce446a653879642efbb4bdc`  
		Last Modified: Tue, 07 May 2024 20:06:05 GMT  
		Size: 20.4 KB (20407 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:1299143e45290f5e63be349b4768b0461bc776c5b2965feb1ab60de05aa18728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76193904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01660941bbd4c1b9eb525bb6042fd217ad8388c04e957b7e354c6b063305024e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:02:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 01 May 2024 14:02:44 GMT
ENV GOLANG_VERSION=1.21.10
# Wed, 01 May 2024 14:02:44 GMT
ENV GOTOOLCHAIN=local
# Wed, 01 May 2024 14:02:44 GMT
ENV GOPATH=/go
# Wed, 01 May 2024 14:02:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 May 2024 14:02:44 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 01 May 2024 14:02:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 01 May 2024 14:02:44 GMT
WORKDIR /go
# Wed, 01 May 2024 14:02:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_VERSION=v0.4.0
# Wed, 01 May 2024 14:02:44 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 01 May 2024 14:02:44 GMT
ENV XCADDY_SETCAP=1
# Wed, 01 May 2024 14:02:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='bd3f08b2fe678b877a3ba23c8801749c513f066f8c2f8fdcfb74cb0cf305a0063e268f44c407eb614b6157d09357913428462153d16b969a2828c1998872b994' ;; 		armhf)   binArch='armv6'; checksum='5011a139379d5d62d5c3bb18037919667e8c9bf98fec1d3e4f5ab6ebe82f43e51d64fdbce1d673085b27a9dd23f41a1991141caf9aedd28ef5956b8147320144' ;; 		armv7)   binArch='armv7'; checksum='06f5ee41eda0571c855d4fcef6f523f892e37b560815f3f5014fe985090173c79d4abbde0efc80d4491d6ac3cfa5609eb220d81a49fb3307b08283c107b81412' ;; 		aarch64) binArch='arm64'; checksum='b730a207efed951846ee322755c16042cc8135a4b3ae10bb550e3801306b3811b75a72f4dfbfdb2bbe38d4247ce30d52051ca85277abafeb50616f6387e6cb58' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='139a13652eb5f16a84cc6dd3255c6822306487cd3414a76fc174fc2d96bde08701abacdbc7ece282e64409876eb946b1665909bb53413cd1b0574ce1eb1eb897' ;; 		s390x)   binArch='s390x'; checksum='a722acbdbf74727e3b8fa14a1e7638b2dbe0e0aeb32c8d5af98fd274cd22bb5ea756072a6f3a46bfc8345503deddb876105cb0f5f935e30fd1525962914ed5c1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.0/xcaddy_0.4.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 01 May 2024 14:02:44 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 01 May 2024 14:02:44 GMT
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
	-	`sha256:62efd05628c84c56ce59fb9fa143673665b3e3952f2f0298347b808b1e2f3356`  
		Last Modified: Tue, 07 May 2024 19:06:20 GMT  
		Size: 1.4 MB (1352119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3592381c919894c9581e34b96cb69c8e98ff5f16440d0a95ba7daf149709f6f6`  
		Last Modified: Tue, 07 May 2024 19:06:20 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:338906f3669707084c3174b53771531218ebdb636e3f5a2ec2b543559978aeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 KB (281438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9734fd17772afefe6b3aedbe3953729d6e556a63db1e494a56045e01a8c6d91`

```dockerfile
```

-	Layers:
	-	`sha256:dc9e7a2bdfbdecb2563594f993c6b20179eee8a313e26d9b083f776958e1e186`  
		Last Modified: Tue, 07 May 2024 19:06:20 GMT  
		Size: 261.1 KB (261094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02ae380ea2aee313ec2fd7c969a7440a93deb1655fe895f644a9ceebf6113fba`  
		Last Modified: Tue, 07 May 2024 19:06:19 GMT  
		Size: 20.3 KB (20344 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:4c217d063b75de6f9a98ec09bc1c333a5aaf61ee7afa8d04c7a69c110bf9f7ca
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096363561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5059d9c48acfdb7dd83c5143c90f54c4d514e059d3b153ba8808437c66222157`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:06:58 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:07:00 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:07:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:07:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:07:59 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 May 2024 18:27:18 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 18:29:44 GMT
RUN $url = 'https://dl.google.com/go/go1.21.10.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '09170b66e7d7c4e2e7a30b8f3350778a8ba5c15951b7eb8ff7545cb86ea9bb71'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 07 May 2024 18:29:46 GMT
WORKDIR C:\go
# Tue, 07 May 2024 19:51:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 May 2024 19:51:23 GMT
ENV XCADDY_VERSION=v0.4.0
# Tue, 07 May 2024 19:51:23 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 07 May 2024 19:51:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 07 May 2024 19:52:15 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.0/xcaddy_0.4.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4798dd7a73be99b4c035816af6f59d807014828bbe45e673a6b79182d3a9ecded48dd453691f02d178481c62787f53b3703e5a4e1d69b2b78cb9644f2e56dcf7')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 07 May 2024 19:52:16 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5ca144c62db12ea36d3f00f6640c6e4758e616b730c3d993fb57c3c8ebad9`  
		Last Modified: Wed, 10 Apr 2024 01:34:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d031792c46321e7a0a81f081515ffa50d7c86201a35780d03b0a1a0ecd68ebac`  
		Last Modified: Wed, 10 Apr 2024 01:34:49 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91b14b8df5887a0feab0adbfcf0dea95d1aab9c3e32619bf6ec5bdc4971a9a4`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099fb3ff689379a9da8dc64f6c1c8d941fb9f0cf66715dc1af16055bdb8e63ec`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ca11c05a0028bb84d4b2b76249dfcce87ea1f22340e50e79681c2055ee1d27`  
		Last Modified: Wed, 10 Apr 2024 01:34:54 GMT  
		Size: 25.5 MB (25528844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f661259fd2478a26bea01012713bd3afd154dfc37f4aafd87ca98d67f75b7`  
		Last Modified: Wed, 10 Apr 2024 01:34:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5830a087830d60f2ed8f1cf87fba9d92cdf7706d61f7692f8aada1a5aec889e8`  
		Last Modified: Wed, 10 Apr 2024 01:34:47 GMT  
		Size: 255.6 KB (255649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf59be8e75cea644ae5a43fb1b4b790d4a4d9b136bd77eef2805999693b104cd`  
		Last Modified: Tue, 07 May 2024 18:41:47 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd70e51e188603f9a571549cfd61deaad21791900bb5523962981fb97beed02c`  
		Last Modified: Tue, 07 May 2024 18:42:06 GMT  
		Size: 69.4 MB (69375754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21570183d5452a6178c68ce062bbdff57be09a14e92dcca4fbc0ffc9afe94f2c`  
		Last Modified: Tue, 07 May 2024 18:41:47 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebc1e5aa22fc661944e9552a3bd0ec6cda6945e654d0f5ccabbf8a581f0691c`  
		Last Modified: Tue, 07 May 2024 19:52:19 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b596305bd9a9b6f9ebfaff925a4dcd901c2bdecbe1261a2bd086ab5f165a6bf0`  
		Last Modified: Tue, 07 May 2024 19:52:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8801e695e868212db4ac8ddfe9f3a87b91480a091042ff75638168d4e14b6f4f`  
		Last Modified: Tue, 07 May 2024 19:52:18 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab0046d6c43a15f39e10ca7ca33a901482c1856664175e2cad38a529bdd37c6`  
		Last Modified: Tue, 07 May 2024 19:52:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c742198a123a0d3b6ff43677c9b462f788894a3fdac39636b84b82b45401f8d1`  
		Last Modified: Tue, 07 May 2024 19:52:19 GMT  
		Size: 1.8 MB (1812014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48938f208175152c2122b9bde073f3799124b511ee65bcee146b7d467477a555`  
		Last Modified: Tue, 07 May 2024 19:52:18 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:8a0ebbad06b9122718baf1979bbb5f22f4884fad3015ccb5f2063fadce18bbea
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261446143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a50b09728da69a74e81194284fbf40f618d6bb6efe38d28e2387bed3de2c8e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:10:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:10:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:10:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:10:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:12:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:12:15 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:13:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 May 2024 18:30:02 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 18:33:41 GMT
RUN $url = 'https://dl.google.com/go/go1.21.10.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '09170b66e7d7c4e2e7a30b8f3350778a8ba5c15951b7eb8ff7545cb86ea9bb71'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 07 May 2024 18:33:42 GMT
WORKDIR C:\go
# Tue, 07 May 2024 19:51:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 May 2024 19:51:09 GMT
ENV XCADDY_VERSION=v0.4.0
# Tue, 07 May 2024 19:51:09 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 07 May 2024 19:51:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 07 May 2024 19:52:58 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.0/xcaddy_0.4.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4798dd7a73be99b4c035816af6f59d807014828bbe45e673a6b79182d3a9ecded48dd453691f02d178481c62787f53b3703e5a4e1d69b2b78cb9644f2e56dcf7')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 07 May 2024 19:52:58 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b97b1625fa02e123dfc05bebcf9f05077e6dbdd1f5253c3c6d07b95f0f55f`  
		Last Modified: Wed, 10 Apr 2024 01:35:25 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6532f7333203cbc41355f91a4431427f575a24ad3dc3dd393b4292b4c2660d76`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c34d692c7e9d5e97e4674c9fefa41e1c78447d2e9c8db3a3f94f325b6188af`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cead4e65b4492e37b01dc6043de135f9dfad18c9f01232c605eb59e7da4a98`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7638380d4eb3933d8241dfe83deaffc516e8bed7b2ab01f96b42864a0d722760`  
		Last Modified: Wed, 10 Apr 2024 01:35:27 GMT  
		Size: 25.5 MB (25535896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159dd7a1de12391b28b5260b6132a515d19e87a7e18b64d7bc843df2c26fb615`  
		Last Modified: Wed, 10 Apr 2024 01:35:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3004df08705794a49d57aabf8c97ae8dfe750cedd45eb476bd574ce29807e152`  
		Last Modified: Wed, 10 Apr 2024 01:35:21 GMT  
		Size: 263.3 KB (263307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5155135be95d0425a26e9a6756eab6fcb7ce32b3da3ec6a9db1485c2c78eff3`  
		Last Modified: Tue, 07 May 2024 18:42:15 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf38e9da6691cf80389507abf857bcfb706187c2b18c4e2a3ab8e4b3063646a`  
		Last Modified: Tue, 07 May 2024 18:42:35 GMT  
		Size: 69.4 MB (69375247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509dc5d2c9595878a2be9c59477fa20f85a091b8487b851002790ce02d2f9ca0`  
		Last Modified: Tue, 07 May 2024 18:42:15 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7838970dbdeef02f21288d6db681e306dfdc01c4dc1ae6cfc9ef622e756b519`  
		Last Modified: Tue, 07 May 2024 19:53:02 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df46a1918824e05097fd94f1b524036902e160317d38fefe99a5b844f615e945`  
		Last Modified: Tue, 07 May 2024 19:53:01 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09235c54ab4d87e6ab2118af9a30d5302e8b6c1c41ec21034cb9fbbcc4e6ac5c`  
		Last Modified: Tue, 07 May 2024 19:53:01 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28654f43884cdcfaa7d06ef6abb025001024fc4de7e69e20fc9f86d8bc5ebac0`  
		Last Modified: Tue, 07 May 2024 19:53:01 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adfa503ae8bdae9fe79a0376d70a98d4b88de51af55749647bec695ebbb71ce`  
		Last Modified: Tue, 07 May 2024 19:53:01 GMT  
		Size: 1.8 MB (1826193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d965ef39a682845e20ce13e9931be75037023f073f2a54a86bec23a1d034ca`  
		Last Modified: Tue, 07 May 2024 19:53:01 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
