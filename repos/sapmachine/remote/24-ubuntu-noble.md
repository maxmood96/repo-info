## `sapmachine:24-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:dde82f457de51a408035890803d9ddbf5cfa78fa21b5b66c65193ed0180b70e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:b078fb1e70a7cdc3139963be13283f35f757770f1343af8eb37feb403c65fadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262145278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbda464fff9c5af50a6a8d6df9dfa5498c83faf062aded12b652da5affa6ff0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f03e71d60a3fd411bf974f1a6a298511beae2ad730d1bfee9aa35eaec780e4`  
		Last Modified: Tue, 03 Jun 2025 13:48:40 GMT  
		Size: 232.4 MB (232429941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:962e462d7a63f19bcfc42ffa1069a07d58312d1d0d0feec048fab00cf4c108c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bbaffa17f08ff86f2bab35d941f821fccebe00f30bf53819f379f82af0dcdb`

```dockerfile
```

-	Layers:
	-	`sha256:58bb0000941f87a50d4e78a02cf4ae61b9ecb6886d2c261e83bd92b650fadc6e`  
		Last Modified: Tue, 03 Jun 2025 04:17:50 GMT  
		Size: 2.5 MB (2489111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c736711824b28bfb1b637a88b671aa8633b1827fc6de2b2af7030871ee8e49f`  
		Last Modified: Tue, 03 Jun 2025 04:17:50 GMT  
		Size: 13.3 KB (13285 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9d8da46b6f0a36f8eaf74c5d3d2ce0e82f21d5f1ad46e47c6e1c6bb280a2562d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259212316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73520ab42db68440cc31efeccecd8718ba2c72f13b3a596115123e169756cec8`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774d3a6234a70719b14242ec6746abbc91d4d06f6f1036f09ac21cb7abf06b51`  
		Last Modified: Tue, 03 Jun 2025 16:47:36 GMT  
		Size: 230.4 MB (230360417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:80e530fc415f5647f14249dd2ea6bb7aa0d30cfbe63a3886028aa50384bac1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abc99f60eb66617d0de7fc5d2ce38e7250a3b68d28544e544937ab71b9ffac8`

```dockerfile
```

-	Layers:
	-	`sha256:791b3f5a1282abe6b6cb27af21f0746932e251bd4ec33a9edf9e54bdaea2fbee`  
		Last Modified: Tue, 03 Jun 2025 05:50:23 GMT  
		Size: 2.5 MB (2489744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f051c01d8d0c77a92008ef146e910b28fdb90169bbaf0b9569f1d551ab9db76a`  
		Last Modified: Tue, 03 Jun 2025 05:50:23 GMT  
		Size: 13.6 KB (13557 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b7bb1c36d0adb0f375398492647305e944aa7989905e1c0c52baff23012804e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268096820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bd924d348c1acaff52b5af721228bfbe55cc8c10f089ca41eaa05a20c8812e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b2277112b5726060395a0370add8425991e766173e2e9d9543d50dc686b71d`  
		Last Modified: Wed, 04 Jun 2025 02:02:37 GMT  
		Size: 233.8 MB (233771610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:78438e291f0e4c00512413185c9fe23a545110b4fd79e9257486b42b22426a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2504117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30caa344376bf5e9bda8616fc88bab3801e862535b31f8c7c184850178579095`

```dockerfile
```

-	Layers:
	-	`sha256:229c6eb90ba8488cc31b5fc1430555bf35d2868c31ab0c6464a78dcbf1a9280d`  
		Last Modified: Tue, 03 Jun 2025 05:42:24 GMT  
		Size: 2.5 MB (2490704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e2772d8b90508f09093268cf091cf8cf7cd8f89bc9aa896de5c4c6e0d49199c`  
		Last Modified: Tue, 03 Jun 2025 05:42:24 GMT  
		Size: 13.4 KB (13413 bytes)  
		MIME: application/vnd.in-toto+json
