## `sapmachine:jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:ff60c0a57c490744609d9ab25b6e2331925096424b31eca4db96f2e4f0f7cc7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:0725a8f4b162c5c56ce8f122e20f7c1f86809f79a9556d7cedf9cf9b3e928bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (99023317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcfd96b613974b9c20aaccbb2c7c8edce08ecbaecbec42d436f363a5813dd3d3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215077fbe1f909a41b53a7df901f5fc86c84fdd5531d8e38880bfefd64273446`  
		Last Modified: Wed, 19 Mar 2025 20:33:02 GMT  
		Size: 69.3 MB (69269027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7815b87a9a2ec6901df216ce9c6f8bca99dbc3e5e04779704160c6d91d20773a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24f67a45e3b47d97c211197e0ce405232808d00b079450fc764ccb949f7b417`

```dockerfile
```

-	Layers:
	-	`sha256:28c7f2ccf0ff7978a48e973b65f7829c6f04524de8f47858de2df07826bd5dfd`  
		Last Modified: Wed, 19 Mar 2025 20:33:01 GMT  
		Size: 2.2 MB (2159153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d06edfb149d4771765b38f27a3b7add9a5b2c6dbdacdbc668792455c90d7c6`  
		Last Modified: Wed, 19 Mar 2025 20:33:00 GMT  
		Size: 9.6 KB (9556 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e8afa10c90a7874914883126cff7d303f69933137f509b8e609c0f05898989dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97016652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b601634870fcd1091bb1cf4720a3403a6d514a472a13c5b18a6f6aa60dcf2680`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39381959dcbe23635ea24af176e6a81805f3abf509d4a71dcf75d14ed8cfe5a8`  
		Last Modified: Wed, 19 Mar 2025 20:35:25 GMT  
		Size: 68.1 MB (68123054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:35c275ac67787ea82b5e05b56e2c233d54fc8477361dd9374ee4ae63e909ac5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab409ff58fff07e47ed6f06391d5cb7195a44bdbfb3722d5cdeeb531fff5bf85`

```dockerfile
```

-	Layers:
	-	`sha256:b780c6637067f32abd2d28e2162f1abe90c206ca8e443d9f73807ff1760816fc`  
		Last Modified: Wed, 19 Mar 2025 20:35:23 GMT  
		Size: 2.2 MB (2159633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97f6fc76668a1084c0ad0829b9b299d426767651cae42d2e362723119fe340a5`  
		Last Modified: Wed, 19 Mar 2025 20:35:23 GMT  
		Size: 9.7 KB (9685 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:35ef2511fddacf059b8cf948bdcccf69723a18426d7023f378f90607f61b7523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105063527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9028351111321824fca737a933736c3daaca7469aae272f80b2d3e4586c6c437`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f035eacba8273898515046e09c413294459618536a2e2064b2163c459698eea`  
		Last Modified: Wed, 19 Mar 2025 20:53:27 GMT  
		Size: 70.7 MB (70673703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a1fb9fce8b84ec94aab349982c9c473f241e34a6204c4ec40d4ede06c651f140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a6742b1f7ba4987bb8ba7ed962f24e3c60034a1d1c165010f9114031a0d25d`

```dockerfile
```

-	Layers:
	-	`sha256:fb9446e0ba7b42d7cce83bee43e66441e68203fc568c16cdb33aa82013b90eda`  
		Last Modified: Wed, 19 Mar 2025 20:53:25 GMT  
		Size: 2.2 MB (2162411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c262d73c4e29858317737580441a0b0c7703d02f7224126c00eea5084da82db`  
		Last Modified: Wed, 19 Mar 2025 20:53:25 GMT  
		Size: 9.6 KB (9613 bytes)  
		MIME: application/vnd.in-toto+json
