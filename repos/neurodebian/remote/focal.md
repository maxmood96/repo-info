## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:f3353bfa17cbe804eb168fe090a431308ead1bdc8569fdd01a3b155f7df701d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:22f4e94698ff19cca859654c30bfdbc5c6aef2889b596fcce3bfd5e463655020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6490391a89e51eb7d46952bc649b6a3ab18926e30ea9f459f376d4b90c48ef0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d5c32b56a7bb4f3bc718412ea8bd648edb0660f1231f7f8e7454518b7b9cc6`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 5.4 MB (5360241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64b1e5dcb5bc5ea11cc316a30022dd544be08e7ff35bff0c49b019a293e7c7f`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ca3b8c895950389becd9bd41f45bc1692e32ad08257b9dc050e454019fe9b8`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f62fa24fc1f5ece4b6afd0dda81f7d6677cacd6f8c2289c7688b0e7daea1c70`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 105.2 KB (105234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f63c65c3b418ae41a5635f8be194cfdf4c957c0b26ea2e8b1e7d2716748fe4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9469e71351bdf024ae1eedc2f364e1c30d8289b20b89a56d6945145683efae9`

```dockerfile
```

-	Layers:
	-	`sha256:24273410e30ea80c582c3b6b7d44dd6d61822ef648ec3684096e1624714774d8`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 2.0 MB (1977956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7713f1a8595ad80b05b7290f60a0f2811f96a292da47fe498dd6cefbc445ec9`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 13.4 KB (13356 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:cd62a88e7cc6f32a69e56635539b1d7f4869713a52ddc8a6983dd1531d64bdd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31424281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57decaed93ea9fab42ff7d7675d598c3be9a7938c1bee75b4cfbc972a46d7e60`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d7044108e6d4d8b24ea68c7ee675f78cb56d959d0878b78c97e8ca7c6b5fa2cc`  
		Last Modified: Sat, 27 Apr 2024 14:55:02 GMT  
		Size: 26.0 MB (25975500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7460069852b1ef3ec3db5c656cd29056ef39c27bfbe286a7c72d2a608ff645`  
		Last Modified: Fri, 31 May 2024 13:01:55 GMT  
		Size: 5.3 MB (5340972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b1f95868daab552a30093084878b1c34eae658c7e27d03ff85f58ae14dd3bd`  
		Last Modified: Fri, 31 May 2024 13:01:55 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc4d62edd5e0d6e0f35113986dbfb423e7b6ccba3cf60b6f66097c863adc6ac`  
		Last Modified: Fri, 31 May 2024 13:01:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaae3ca4103434ee2ff24850cb155afcd19e9e97796af3dcd6bbee0367ea4e2`  
		Last Modified: Fri, 31 May 2024 13:01:55 GMT  
		Size: 105.8 KB (105814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d7ee03dc8973363ebb86a73a986da2e6984bd4384255bbfb605dd2eabd4663dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff131642289b942cfe715cd0b55d90565a852178446c630df36201d0da69269a`

```dockerfile
```

-	Layers:
	-	`sha256:f800a335ea081d41adf81685726e31fa3b9eb294349f1d36f18e460cf89cb61d`  
		Last Modified: Fri, 31 May 2024 13:01:55 GMT  
		Size: 2.0 MB (1978184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:276cf0b9d2d592eabd6cc18483498b6dd30975a243ba09c16f22bcd0d1176682`  
		Last Modified: Fri, 31 May 2024 13:01:55 GMT  
		Size: 13.6 KB (13634 bytes)  
		MIME: application/vnd.in-toto+json
