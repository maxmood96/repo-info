## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:ca0411863c9bc1c15a43608adc6c813ea3840e78518cbe68f85adedc0f72b29c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:77a20a3dad43511f345f00c838fedb633f49165415d670f5d70b9927e3d37426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7570a3bdac51817091c1f2918805ace346e066f57bdca6fb85b315ad61a84580`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b6f830cd306f01980373f1e0120f2d00018fbe51a9506b7262f5d9e4bbda74f9`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 53.8 MB (53756115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50565ea1f5baca150b83f4bba60eb266d0f5d6b7b7e09c8b1a243ce884208fa`  
		Last Modified: Tue, 21 Oct 2025 01:47:25 GMT  
		Size: 11.1 MB (11105047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079d12219a647c0cdbbef523d0a1da4300cd7cb97ffbad82a4c6a840d5833b83`  
		Last Modified: Tue, 21 Oct 2025 01:47:23 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff5c2ca4e368b9bb499af345fcc54f66dd6edd7b42b465fb44b538e9a3db9bf`  
		Last Modified: Tue, 21 Oct 2025 01:47:23 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575d55c9dc98a812a0feaa11b59560e42ebfe95a1667cabcb3090db8cf4f30d8`  
		Last Modified: Tue, 21 Oct 2025 01:47:23 GMT  
		Size: 101.3 KB (101332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703a09e70b2db05e2533b2855cf278b24d2de1e5d4425ce7babc577eb97eea14`  
		Last Modified: Tue, 21 Oct 2025 01:47:23 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9c1ebfe9ad353640cd54668877067463f4fa4da9127613ffbbfa9f9861214f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3686f843c85ab66bb74a221baa82c4d2f7f733eeaf22d642a5c0df42916ad9`

```dockerfile
```

-	Layers:
	-	`sha256:74b6302aecbae566269eb6f14a5c85eb9f1d27de806324f7ac977ca62c0f5e4c`  
		Last Modified: Tue, 21 Oct 2025 10:07:59 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b96481a27cf1eabe119f144fcd4d6a402f4aff2699c810702068f63a1be89523`  
		Last Modified: Tue, 21 Oct 2025 10:08:00 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6d91df3d740700fc6c5534ff5d1f325fc4ebab5f2320769cae24c2da8e7b1cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba397c54db80647edabf9fc47248929507dbea060a38095c6214688c01b13bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0a72c4e347b74aa6a0086cf3d1d928528ab02577a17bff4e22366a7df681f564`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 52.3 MB (52257444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb83c78b93803521647258c4b1469c60e2fafbc0bbdb0ca7e79d5a8b6687afcf`  
		Last Modified: Tue, 21 Oct 2025 02:30:55 GMT  
		Size: 11.1 MB (11105962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92c8a3c5ddb6630959142243cba561c63b3873294e0c96577fb79370ddc322a`  
		Last Modified: Tue, 21 Oct 2025 02:30:54 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f495fda5ebdce32248f23379de3070daf336202a04c3cae1d203c280679c07`  
		Last Modified: Tue, 21 Oct 2025 02:30:55 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624d43b2a69204c8e4ee85efe152f7372eb6720a145f9f14c49462045fe2f50`  
		Last Modified: Tue, 21 Oct 2025 02:30:55 GMT  
		Size: 101.1 KB (101105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1310863e5772dca8d286a5dc66df8067a57739edab214c2cf08926fcefc3eb68`  
		Last Modified: Tue, 21 Oct 2025 02:30:54 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f1b32259622b2402e11ab41ef3e9e34ab6a25715fb4f4315d205d9ca4c848cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc008ed0e64145cfd789a700706236fb4d670d3ab2686a4b1046b2029b735d4`

```dockerfile
```

-	Layers:
	-	`sha256:2088c18e6b6c4687a1467428fe3e66b6c06c3de375efc09254a7fea12f48ce29`  
		Last Modified: Tue, 21 Oct 2025 10:08:05 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eb4a0f8ce521001c24f3b95debbfd5f1b77ba164c802b1c5af0815b7356270a`  
		Last Modified: Tue, 21 Oct 2025 10:08:05 GMT  
		Size: 16.2 KB (16175 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7fed942593aa7599211e70f75e5b492b868702120dbc489762215ce4efe86234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a09f49358031d42bbe99ee1f2faa6cf41ffa0547f8080b872a1f75786d115a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:10d430deaa3d2ab4898db053e80d62403503897839bf6efd17ed5412b18d7973`  
		Last Modified: Tue, 21 Oct 2025 00:20:39 GMT  
		Size: 54.7 MB (54699294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bafb03c492417d745fe9148c731122a53e1f35f9af2e8df8bf69ac48cb9b43`  
		Last Modified: Tue, 21 Oct 2025 01:54:45 GMT  
		Size: 11.5 MB (11500372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73ed3fa36e6e8124959f4c297f50987f6f26142fd6ec0135d10cbdf5dc86fed`  
		Last Modified: Tue, 21 Oct 2025 01:54:45 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c87760869e26f5be49f48136d1baaad65f589b757cbb756f3f51cfbd8230252`  
		Last Modified: Tue, 21 Oct 2025 01:54:45 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9f7cbbfd83d93b1c49793a29f52b7346dfdf69670d3f245e2fe6578048aeed`  
		Last Modified: Tue, 21 Oct 2025 01:54:45 GMT  
		Size: 101.3 KB (101268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9144282a34d8df12bfc67bf3144965b65798d910a7f379d9c2fb8dba752e0a15`  
		Last Modified: Tue, 21 Oct 2025 01:54:56 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2926deebaf841068578829c7a1023439cc2ca1b424b56cdfebec40900dbbfb05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e60728a066824c137f2594e7b11d9cabbecfcacb30c1a6c41dfc7fbeaad101e`

```dockerfile
```

-	Layers:
	-	`sha256:103253e8856f4e22885d260cc0150762d549dd551f4e144dff6d7a37a611c65c`  
		Last Modified: Tue, 21 Oct 2025 10:08:10 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22d61da499d3a917962bea9e31d00fe1fb3d22be57f6cd85663f0d5b3e9fc865`  
		Last Modified: Tue, 21 Oct 2025 10:08:10 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json
