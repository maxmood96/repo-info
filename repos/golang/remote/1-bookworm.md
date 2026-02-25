## `golang:1-bookworm`

```console
$ docker pull golang@sha256:878786d2372335058513ce271a4a5c2a1d3e6839b105144183464a05558b101c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:4f7e5f23bfacf4c2934ba70c132532742b6a53f01a4209e2c2eb7bd06c16f0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296544622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9789e28a041a0954109edf258ac214e503059ce1b294cd5d22f908eefd508c9c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:39:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:39:18 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 24 Feb 2026 20:39:18 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 20:39:18 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 20:39:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:39:18 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 20:39:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 20:39:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa27031269f0a970255d56a9e793fc2a9d6bb091463cd5e632af4ae274881601`  
		Last Modified: Tue, 24 Feb 2026 20:03:49 GMT  
		Size: 64.4 MB (64395853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bfd5ef2e8868ffe266600a5cff44e069ddb54d45eb5f430b9301c92294105d`  
		Last Modified: Tue, 24 Feb 2026 20:39:47 GMT  
		Size: 92.4 MB (92444714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ede2856567d2593950de6f98f5d2763ae304caeb0ff577a1318c065a8fd650c`  
		Last Modified: Tue, 10 Feb 2026 21:25:34 GMT  
		Size: 67.2 MB (67176670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6449dbcf05ba7c3634b4d6506104e038745369d52d4fa693d1a880c04aedd0`  
		Last Modified: Tue, 24 Feb 2026 20:39:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f127b619c71654cd2514a9f37fd15b2e54f1bde8fa773eb11b1b3d8c79379d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435994bbdc13449a372f313bf5529f7e3f9d6f1e4e66a99cc8d6bce8abc55945`

```dockerfile
```

-	Layers:
	-	`sha256:a968ddd649081f762bb0ba800015887deb780fe2402ccd59c4a335e0e5224e73`  
		Last Modified: Tue, 24 Feb 2026 20:39:45 GMT  
		Size: 10.5 MB (10497855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3a9c55284a1bf71c36039e2727f5ccc1651dc9e53c655a8cb6c07906cda477f`  
		Last Modified: Tue, 24 Feb 2026 20:39:44 GMT  
		Size: 27.8 KB (27796 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:e307f2bd99e40f61c08b6489ad17615058dd9242a8542d1271bf04729c9aa9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257845287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf604567f3f8b00919c4c3e8b84eb3ef5c8db1eb99d4ac286465d9f40ba21dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 22:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 22:16:12 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 24 Feb 2026 22:16:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 22:16:12 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 22:16:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 22:16:12 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 22:16:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 22:16:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:510542cb38bcb0c99cf41f8715bc80ae2e63df19b8399efbb11254ee0ddd4299`  
		Last Modified: Tue, 24 Feb 2026 18:41:53 GMT  
		Size: 44.2 MB (44207818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122a79376a0d51f606a8d45c17043adef288961e7b30a2332c485fac0427d825`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 21.9 MB (21942084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9742857c89c3fff9f983a1595594994ae63f49f2e0dd92faaa9d5886d69aedc6`  
		Last Modified: Tue, 24 Feb 2026 21:34:25 GMT  
		Size: 59.7 MB (59651871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8da36d2a3ec149cbe641d2d4f67754bb95549e37e64dd61b96f51c5ed79766c`  
		Last Modified: Tue, 24 Feb 2026 22:16:38 GMT  
		Size: 66.3 MB (66310471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb468d6c3aa96f0258422956f98c08c3bc799ec9552ffdc9be6851ba4d40573`  
		Last Modified: Tue, 10 Feb 2026 21:25:20 GMT  
		Size: 65.7 MB (65732884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca664c9373ce5b45620c0ab0615840e530600e3eb3db6083671783ade4846cd9`  
		Last Modified: Tue, 24 Feb 2026 22:16:36 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:92c78e57889a8747db967ae581f0fed3b0f10084005b435338ce74078f98d3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec1a054433141ed9aa2259d5597427fd421778b312a269977b69ebc46105a58`

```dockerfile
```

-	Layers:
	-	`sha256:2c356900daf71d2c59a5f91da0e263c8815745562d5ce0743ff853f388642769`  
		Last Modified: Tue, 24 Feb 2026 22:16:36 GMT  
		Size: 10.3 MB (10304567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a2cdb86bb782838872d83efe9ae29af4a4af3362b3a2df971623930b9e28dad`  
		Last Modified: Tue, 24 Feb 2026 22:16:36 GMT  
		Size: 27.9 KB (27903 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:1ee99c345f8179002a0de40728e0eaa8865b81257b3924ef150ee65b3f1d3fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287066720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61612546a0234a63159cdde84460c27cc10bcc24052ba6ddbaf7b089843a71fd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:14:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:30:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:30:12 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 24 Feb 2026 21:30:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 21:30:12 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 21:30:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:30:12 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 21:30:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 21:30:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d27b842bb73f4af595ce58848c4c53ae713ca5c649636d25b483ca63bccc52`  
		Last Modified: Tue, 24 Feb 2026 20:14:46 GMT  
		Size: 64.5 MB (64479406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d633f8c312f6bceaac8309800a4139faffb66163ee1f9a3596dfeb0c251980f`  
		Last Modified: Tue, 24 Feb 2026 21:30:40 GMT  
		Size: 86.5 MB (86525207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5a418ef96019867316412a90ec8973c4ade493b1d6671994ae31514a8ef6cd`  
		Last Modified: Tue, 10 Feb 2026 21:25:38 GMT  
		Size: 64.1 MB (64084003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46ed6148976ea0df8fac981a2424df97a665a990df4e957f8af37e4354f54ab`  
		Last Modified: Tue, 24 Feb 2026 21:30:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d9b2dae4d4b66b21f8b27e1b8a9c1400032a6aa3b9fed4170be7b6085be767bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e527319cd9e13b33eb3993bff8c0ece8836d1ae0aebc4a3703f7d224491e21`

```dockerfile
```

-	Layers:
	-	`sha256:0ceaf8b3535fbef28ca6986aa736e9206ae856fae8484dcf80669f045abe0b84`  
		Last Modified: Tue, 24 Feb 2026 21:30:38 GMT  
		Size: 10.5 MB (10525703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91fad19d56b04f4be35d8e05ccf6b485153f6ea6dbd279cb1051cccd79045698`  
		Last Modified: Tue, 24 Feb 2026 21:30:37 GMT  
		Size: 27.9 KB (27931 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:03a59be226b17e0533ed273bc56066cfd24f0d4e00b043d4622a4a117601e3a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (295977780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c8b1716be57768478af0f949386525784412a17d412b3a1badeea1d4a8974e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:56:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:24:42 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 24 Feb 2026 20:24:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 20:24:42 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 20:24:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:24:42 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 20:24:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 20:24:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:443394a7d911f581670ce4df7959c82f7e8f0be02b5a7ba3c71bc5958012963d`  
		Last Modified: Tue, 24 Feb 2026 18:41:48 GMT  
		Size: 49.5 MB (49477853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31e1fab6283d72f6ce2de137bc123a8ab89a85f0baa0b6c11c2c6d28c359a32`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 24.9 MB (24872106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383bd8d2ca9c40d67394c0121b8fdb7d7c8f44082342e21f4188fc611c88e9a6`  
		Last Modified: Tue, 24 Feb 2026 19:56:53 GMT  
		Size: 66.2 MB (66234334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8de6a3322cd37fb0626f662e5edf66445ae36e30eec5699a77cc887ca1f35d`  
		Last Modified: Tue, 24 Feb 2026 20:25:13 GMT  
		Size: 89.9 MB (89871593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbfad3c600a3a9c8302db25d37648349b37e769601e5490f9bfb9f615fe5677`  
		Last Modified: Tue, 10 Feb 2026 21:25:34 GMT  
		Size: 65.5 MB (65521738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529eaff489d805b2fa0867467a7a920df6425d4f6445bdf007f2774ed007f588`  
		Last Modified: Tue, 24 Feb 2026 20:25:11 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:432cdb6f5115b296e774dc0f8f7e85c70f9e74ba2b554933181434364be5360a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10505186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f8c574e7810d431e00ac70094e9b755210e073230ef4c041a98c84add3df6a`

```dockerfile
```

-	Layers:
	-	`sha256:134ba95d23359ea5e475168cf2e4e032f59265eb06c3e7d3cc4bb290b8228391`  
		Last Modified: Tue, 24 Feb 2026 20:25:11 GMT  
		Size: 10.5 MB (10477425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e7f9d108d276682ae2e3f8d9ca01a346b45b8556d07c7afdb1934d93ff3bfee`  
		Last Modified: Tue, 24 Feb 2026 20:25:11 GMT  
		Size: 27.8 KB (27761 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:9f780f355c0f1275157775294b076a0a2eb2b3c4b133d6e0c9b5c6d3c55ecb26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268490029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aeb0f571db5abc98843f1b3861d825d26ecb660de8701e7be90248259f60301`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 16:06:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 21:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 22:18:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:24:37 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:24:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:24:37 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:24:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:24:37 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:24:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:24:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:001d31ce76be3df3174382025b0b9e2985ddc96d785143497e14a46cdcdcf951`  
		Last Modified: Tue, 03 Feb 2026 01:12:32 GMT  
		Size: 48.8 MB (48763257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e910e12f1ba466db5d640f799037fd1161885165d6ef1a46de53b55b08cfb02`  
		Last Modified: Tue, 03 Feb 2026 16:07:24 GMT  
		Size: 23.6 MB (23615398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e0ad746711a3754afd4dc1df1be9308a858da3b48f46cc1d318cd1dbf2cb47`  
		Last Modified: Tue, 03 Feb 2026 21:29:58 GMT  
		Size: 63.3 MB (63310108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2164c80380b0dcd60ea92fbd5645d9478bdfb6a0b5dfaabf0daa2a974ecfb949`  
		Last Modified: Tue, 03 Feb 2026 22:20:18 GMT  
		Size: 70.0 MB (70021714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f4b21db9e8b72856ef3b37b567c6f4eaf21673d1c15aba8838a49684db0da7`  
		Last Modified: Tue, 10 Feb 2026 21:26:36 GMT  
		Size: 62.8 MB (62779393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0cde1fd5f96d21451bb13d246f09ba2b435654879b64124320a2d051f8d71f`  
		Last Modified: Tue, 10 Feb 2026 21:26:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4678b14828832504edb4dcdf80e0728c8b038142e948a661c1a4e6471e63774c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8291d2de63586ec24ca972167a828f5a57f1e56ad63a426a6b4b1e8da018a8e7`

```dockerfile
```

-	Layers:
	-	`sha256:da10963ec69a683b6fbc78778ed2f6b08a26764a00aeff9675b3418307f11e56`  
		Last Modified: Tue, 10 Feb 2026 21:26:30 GMT  
		Size: 27.7 KB (27654 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:beff6e12e840b062c01930d166d560dad658de8b6d5cbdd739c932348ed56490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (303036821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac016a879284c9657be8868860b638b161f97a269d033edcce129e1fb3c808b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 02:56:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 06:24:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:24:27 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:24:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:24:27 GMT
COPY /target/ / # buildkit
# Wed, 25 Feb 2026 06:24:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 25 Feb 2026 06:24:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ba53e63c4e3e4d88f0425bc79a37e364db9aabbff9c13ece5cecc63ec880f3`  
		Last Modified: Tue, 24 Feb 2026 21:19:17 GMT  
		Size: 25.7 MB (25671399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5eaeecfe60befcd3d5daac43038587e48eaaea46a2b5f8466018b05c5579686`  
		Last Modified: Wed, 25 Feb 2026 02:57:13 GMT  
		Size: 69.8 MB (69846164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b584ac824ed9aa87da1e6e9fa0340abc1c0ac5e521b4a3a2abf71b0e0b13ac`  
		Last Modified: Wed, 25 Feb 2026 06:25:22 GMT  
		Size: 90.5 MB (90451700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb65e50af4c9d9d06b20c69b0731fa5479387927e011d4a6cf02c0de9c35733`  
		Last Modified: Tue, 10 Feb 2026 21:25:51 GMT  
		Size: 64.7 MB (64730602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4437e7a243929b21d8aece2d0c02bb4e7d264b94fedf6806829c8579d2700f96`  
		Last Modified: Wed, 25 Feb 2026 06:25:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6e557fdca29153f7a88cc694117a12486d6bc8d2b08340681d534e2d7f93b118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10498024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3ffddce45f65b9b1cddac13f3ec1698a926a3c1ad0786106c9d56d35093357`

```dockerfile
```

-	Layers:
	-	`sha256:859fdcd44d1a9094103d9358113d8d8bc2811e07d35714f52fc4af50efe92ac8`  
		Last Modified: Wed, 25 Feb 2026 06:25:20 GMT  
		Size: 10.5 MB (10470352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24666e248653275d7130260444a4d9e953e4896d7c979ab384d9adccbefc0c88`  
		Last Modified: Wed, 25 Feb 2026 06:25:19 GMT  
		Size: 27.7 KB (27672 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:d9b87cb7603d984097e53395486ed380e1afb821314327025590c87abaedf92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.1 MB (270121374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e738fcb7ff6450a02e59480b4c1271fbc1ff2bc857b46e1d08c9f4312812dcc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:28:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:00:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:24:12 GMT
ENV GOLANG_VERSION=1.26.0
# Tue, 10 Feb 2026 21:24:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:24:12 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:24:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:24:12 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:24:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:24:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3072e3eb8c224dc593a4e18a3785b06d51467102b1cd9dd426d3d31d0e6831b8`  
		Last Modified: Tue, 03 Feb 2026 03:44:33 GMT  
		Size: 24.0 MB (24033633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61724404ca7e7ee67a943113b2e679af71546a07f66af094570e811bbc9fa743`  
		Last Modified: Tue, 03 Feb 2026 05:29:11 GMT  
		Size: 63.5 MB (63501320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be60f9687e53e1d931599c2c97d67403bb6a6a87fba5a8672d8f14c72b51e5e`  
		Last Modified: Mon, 09 Feb 2026 20:00:52 GMT  
		Size: 69.0 MB (69045163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0267cccbf93e93da2ed1297ad6771262243fba5de764f475d84248f8d84f3c28`  
		Last Modified: Tue, 10 Feb 2026 21:24:50 GMT  
		Size: 66.4 MB (66402757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fd64ef6e056560c7e86ccd7e2ab07ab01bf15e5bd3af2790908475a5799625`  
		Last Modified: Tue, 10 Feb 2026 21:24:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f7f87fdd64f648cd0f07a84dc94efbb8352131131432a585d442f07c6fbaf1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b94e49dba678c30391860e1ff438e1c002333e2076ab0fee204ff8cd8ae929`

```dockerfile
```

-	Layers:
	-	`sha256:d048057d6bb59579dcff0facbe5ad253673531379b9c8552473c4ebc8418ed49`  
		Last Modified: Tue, 10 Feb 2026 21:24:54 GMT  
		Size: 10.3 MB (10329613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:614e128480d136d8dcf7c7ece3cee62d477b87e83fe6450677714edb08ce4e2c`  
		Last Modified: Tue, 10 Feb 2026 21:24:53 GMT  
		Size: 27.8 KB (27796 bytes)  
		MIME: application/vnd.in-toto+json
