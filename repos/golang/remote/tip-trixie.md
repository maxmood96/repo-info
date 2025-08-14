## `golang:tip-trixie`

```console
$ docker pull golang@sha256:98508216520f0ef7498fa143a49c9fd2f4f901f7f981ba07ec5f18937020b46c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-trixie` - linux; amd64

```console
$ docker pull golang@sha256:fd22468b3153879f924e51ac7f2649a19b5194a12f6aebd8bcd65c6971527837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 MB (327791690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259700ac83069835e852032edd2ffa7b0ba273f014485c4864dec761cb66abb7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 17:45:50 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 17:45:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 17:45:50 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e4db86de6eba33869491caa7946b80dd71c255f1940e96a9f755cc2b1f3829`  
		Last Modified: Tue, 12 Aug 2025 22:14:12 GMT  
		Size: 25.6 MB (25612940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea45766c6449310ca2fc621a7e00bedb4b9b803a7fbfe2607efce6d2e07e435`  
		Last Modified: Tue, 12 Aug 2025 22:15:03 GMT  
		Size: 67.8 MB (67777316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411f287f780c5d97b680191c406ca3be44abb08e085efdc82f5449d0ea1fa240`  
		Last Modified: Wed, 13 Aug 2025 20:30:10 GMT  
		Size: 102.1 MB (102055315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e70f62131fde5fdbd86a9a07a13b0d6d65a669fadfed0d46fc45a0e67fef05d`  
		Last Modified: Tue, 12 Aug 2025 18:32:41 GMT  
		Size: 83.1 MB (83067681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7e13b644b36d8faa229381040e1461a689288a201561af313293841b0a174a`  
		Last Modified: Wed, 13 Aug 2025 18:12:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:9caf6e7b03ed8a2745a7ac8ffa7d4e88a0c42ebd3aeafcd74b81e9ade2b27f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10805949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb450b6f5fe81e510a753eb84c8cf25a8eb53eae6811c7de2308c17fc984004e`

```dockerfile
```

-	Layers:
	-	`sha256:b5a6c6008afe0adb50714a106e0c7f038833f03d4d5ffe9f25c3652be84083c4`  
		Last Modified: Wed, 13 Aug 2025 20:24:48 GMT  
		Size: 10.8 MB (10778310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7640b9205b3eee4fa7389b320b47c64d2417a5ddfc4626d26be547d5fcec00c3`  
		Last Modified: Wed, 13 Aug 2025 20:24:49 GMT  
		Size: 27.6 KB (27639 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:82d53d8614b898da3619da2df8315f4b5ca40939ee4f3cf1a282411fbb70ac40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284823866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeffe6482e68d38495fc4901f4ede3d15a1782d173fce1bc5633d762bdc2e525`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 17:45:50 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 17:45:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 17:45:50 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:58382c67f397ebdc005890f56dc436f7798aeeee2e0d603ba02e89d6243c138b`  
		Last Modified: Tue, 12 Aug 2025 20:51:59 GMT  
		Size: 45.7 MB (45712631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72873bc1bfa1e9338237d9573d1640f6647f61a1636bbd71d8128d16503087`  
		Last Modified: Wed, 13 Aug 2025 00:16:54 GMT  
		Size: 23.6 MB (23613045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe0a58e6c2887b271354fa2e1067ff7e829f063163f76c4a3d4f1da179eb22e`  
		Last Modified: Wed, 13 Aug 2025 06:50:21 GMT  
		Size: 62.7 MB (62718501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bf1e0378255d85ce69e42b8c2b4e52765a17bb9940e69e2993debcac329de3`  
		Last Modified: Thu, 14 Aug 2025 05:24:37 GMT  
		Size: 72.7 MB (72699087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331d10df13da6c65403fe5e3b6a9cc280dde2bb564435b287f2b85119c986cc8`  
		Last Modified: Tue, 12 Aug 2025 19:00:44 GMT  
		Size: 80.1 MB (80080443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb202695251e855d32e594376e315734bb99cf4d81e1d5c2f2b483468364331`  
		Last Modified: Thu, 14 Aug 2025 06:01:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:79f1860dfcdfa02ee107e1c0bde6e122f8c14750ebbb7dd89ce131076fe9336b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10601958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e546cc11ac10c0a2346f914a7ca3b1d7f3b93cd7c5a758988cbd5ecca353cb`

```dockerfile
```

-	Layers:
	-	`sha256:d99e73ff9db72046cfb1b33404ae3d5ed3a7977536d62865293c665577e5fa5d`  
		Last Modified: Thu, 14 Aug 2025 08:23:41 GMT  
		Size: 10.6 MB (10574199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8439e0e9ad0b83998b14baa85d767ba8c10aeb04ffdc079d9fce57134c714f1`  
		Last Modified: Thu, 14 Aug 2025 08:23:42 GMT  
		Size: 27.8 KB (27759 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:af73adf278838efa4fcdf5bb8750cce8dc89312cbc5794fc8b4989acb950bb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316037681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48551d6df15b7b9d3a04f94db52e19b8a17de8268da414480386a248148c6092`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 17:45:50 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 17:45:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 17:45:50 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9923852056eb09462c3344515191318e7aa33ff28057c946bc41a414ee57df0b`  
		Last Modified: Wed, 13 Aug 2025 07:30:07 GMT  
		Size: 25.0 MB (25014610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcc8bff74cbeacbac9c6869b6a9def273b93cc67de196b347688de2a9185de0`  
		Last Modified: Wed, 13 Aug 2025 15:31:50 GMT  
		Size: 67.6 MB (67593628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf37d0607fbadafadb0268414200aa6130cd6c0bae8f71fd256b7b553f69c7c0`  
		Last Modified: Wed, 13 Aug 2025 23:02:50 GMT  
		Size: 94.8 MB (94782268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87b7cf68665eac7cfd64f5bb944a8b17de913d4de7e1d26ec5a73f422afb207`  
		Last Modified: Tue, 12 Aug 2025 22:36:24 GMT  
		Size: 79.0 MB (79005413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6ae4e509a780bd7dc144103dd833c8d3cc8a94441376bd45d35df73824d321`  
		Last Modified: Thu, 14 Aug 2025 03:41:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:cf4f917e65cbb788296c0c9bfeb70e7202cf4b8825432431c266905884997b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10904756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9e2ef6d083871b5460a7318708d53bfe2d2419a597cb024223a5f6b30f6808`

```dockerfile
```

-	Layers:
	-	`sha256:f4683cd691c9c05114df40d4a9543dfb943ccda546293c6c51ea0f7b73a93fa4`  
		Last Modified: Thu, 14 Aug 2025 05:24:14 GMT  
		Size: 10.9 MB (10876961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7544ac28f2f6ba729cf7094de13bf26545917b45e1ada93b04193eaa7a0448c3`  
		Last Modified: Thu, 14 Aug 2025 05:24:15 GMT  
		Size: 27.8 KB (27795 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; 386

```console
$ docker pull golang@sha256:d46f71642d4d705ba2764b0faf1cca46fc677f9c5d5faeb828bf1ec0e3f2cc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329554179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4531d5d0ea902310e88b7dd6e4f0858acc24b3c23cd5d2a5a6a34149fa6ac7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 17:45:50 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 17:45:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 17:45:50 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d9f8c7ff550056ffe2cca57d7110ae0306e74220a891574e97ddc10ba49823d`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 50.8 MB (50794258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde29e7bc69fcf496b5e5df92d7d82da6ff9f4877784085c4dcba73f6ee6a1ea`  
		Last Modified: Tue, 12 Aug 2025 21:20:38 GMT  
		Size: 26.8 MB (26772559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9904337df106e0852d247e06047929e66d5097f2d2c13861e2e31ecc63f4b`  
		Last Modified: Tue, 12 Aug 2025 22:15:57 GMT  
		Size: 69.8 MB (69794753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f45da26a30ca1e7c1ce0133a91f461e7278ee8764dda55772d070858617963`  
		Last Modified: Wed, 13 Aug 2025 18:13:27 GMT  
		Size: 100.5 MB (100498620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be820729530544d2d8ea257bf2456efd73f0f38ff4c7f538f538e091c491a7b6`  
		Last Modified: Tue, 12 Aug 2025 23:30:08 GMT  
		Size: 81.7 MB (81693831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcad8777dc3686c0e4e368abc46e0552d48d7a4e4b3388c58d78b6995a9150d1`  
		Last Modified: Wed, 13 Aug 2025 18:13:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:cbe576b6fbf095d24402d37a13ab8327a76490b94f9b1bba175c46e16272f1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10777172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7296af3393c05941d61b917ce591f88cb71414f412ad570e5c8fa1ae4795f6f`

```dockerfile
```

-	Layers:
	-	`sha256:c80760fb85261ac2a2ad2de24ad8857976e5ef3a3f650fb307fba639ed13eff2`  
		Last Modified: Wed, 13 Aug 2025 20:25:05 GMT  
		Size: 10.7 MB (10749576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6764e6bd23c3cdee83201e2c17152ac85613a013525d9740d220b383ec6c7160`  
		Last Modified: Wed, 13 Aug 2025 20:25:06 GMT  
		Size: 27.6 KB (27596 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:05a911bf3424898d6510280e77d40ce19c25f8214755a892f2b4330c974ed099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 MB (326278855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f6ef2e7eb88adb0cf9ddf3153168f919d0ed88c06cf070762905d178ef34f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 17:45:50 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 17:45:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 17:45:50 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a327675583423e2c44eae4c02a88be15dbeac36073deb88700ba487e0c0e35`  
		Last Modified: Wed, 13 Aug 2025 15:15:16 GMT  
		Size: 27.0 MB (26992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf20d9e1e5f16d7552d637dd4a12484b22e52928311f81dd13c82b6838c2ae7`  
		Last Modified: Wed, 13 Aug 2025 21:23:59 GMT  
		Size: 73.0 MB (73018659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8871c45a7119988c7d962199f82d487aefd5e752fd9f98ec06c4c6735662dba`  
		Last Modified: Thu, 14 Aug 2025 05:07:23 GMT  
		Size: 92.8 MB (92760751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d949d12b56c803641dc1ee823fe0b4254f92598b51ea3dd4b12bbfc422e9b7`  
		Last Modified: Tue, 12 Aug 2025 23:22:22 GMT  
		Size: 80.4 MB (80403035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e763a616804729867492ef98d511e6c10c20ff54bd65d0d3265c310dd30e334d`  
		Last Modified: Thu, 14 Aug 2025 12:00:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:57ff5c4acef3bda1e10e5958acba62bc78ccede7a113ee8b102fcca70f85b5b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10801787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0091ea168c91daeb39654e0da8824fe30099e30c200d8e591932f210e1f821`

```dockerfile
```

-	Layers:
	-	`sha256:b3b1f0387f8fe930d6613faea9d1d85157b0fb7f52a58d1102266b01eaa21b52`  
		Last Modified: Thu, 14 Aug 2025 14:24:34 GMT  
		Size: 10.8 MB (10774094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a10a848c82cc5d17d38045f1d208d0c29c8f87fc62b2c5ce78c8f33b59b3f314`  
		Last Modified: Thu, 14 Aug 2025 14:24:35 GMT  
		Size: 27.7 KB (27693 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:f9c7e4e117b68ffeb48c65163e18653d2367250274d65c6d74d1c9c1a9ad1113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302236255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0a7f0a33d64d2a29ff59b9ba5db79f1420ef50e19e47e17e7757fe0ee23e70`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 17:45:50 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 17:45:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 17:45:50 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 17:45:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47181ddd75754adfc74e4f58b4a898ec33ad906976b71219b567efd19470677`  
		Last Modified: Wed, 13 Aug 2025 03:27:04 GMT  
		Size: 26.8 MB (26779580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415f63d435cf750f4bda1af6afa07ce9f812fa19c74e6f9f050da85f47eb36e7`  
		Last Modified: Wed, 13 Aug 2025 17:21:16 GMT  
		Size: 68.6 MB (68619998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e8a5c04d7aeadb022d07f505d9b83a50ffd376444c5e618b1f58391961e8e9`  
		Last Modified: Wed, 13 Aug 2025 22:24:01 GMT  
		Size: 75.9 MB (75869997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e557abe2162386c1768ffea94bd0b2e886c5afefd7b5aaadb4e3de900ee87e0f`  
		Last Modified: Tue, 12 Aug 2025 18:48:02 GMT  
		Size: 81.6 MB (81621362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75661aff24b5064a285ddb9aeb42546e030b6fc556f6091263633e63a62f7577`  
		Last Modified: Thu, 14 Aug 2025 04:14:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:6e4b29a4a8ca3e201222905d301a6527f6117321fc8bdf44d75c4a440d2e98d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10616345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52df166b486f05563e5794b3ca3f6d08c79b5e323763cd9d5f6b7d2c7112a128`

```dockerfile
```

-	Layers:
	-	`sha256:791be6861b5afe4a2ebc33fa25f63f5f01b8f95ae9e6e57abc361c148a157c7d`  
		Last Modified: Thu, 14 Aug 2025 05:24:39 GMT  
		Size: 10.6 MB (10588710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40daae3d6697898b5b9b138719d44abda9603b9cbac5a509fcb501786f48527b`  
		Last Modified: Thu, 14 Aug 2025 05:24:40 GMT  
		Size: 27.6 KB (27635 bytes)  
		MIME: application/vnd.in-toto+json
