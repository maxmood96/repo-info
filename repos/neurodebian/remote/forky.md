## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:6875d2f1bf3b0fd2ea0480353d060d7cb0904f96590e64891aeccd36af21f2ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky` - linux; amd64

```console
$ docker pull neurodebian@sha256:2302018712146863aeb4690550a5b76df8b7df13e0d802be71a0c3c38149a135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60548458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec708323e8e211beffa0a80ae7bba5f384b434ce88123b60733a0d195d8aa7b6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 00:03:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:03:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:03:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e1869079ab5cc3b00301445717c112f3ddb9424b5d7b2a41713bc70d9482ee85`  
		Last Modified: Mon, 29 Dec 2025 22:28:05 GMT  
		Size: 48.8 MB (48830058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4e5a600b42af7e7249a38577cc844cd06b82d1f22fca446507bc4d97304e37`  
		Last Modified: Tue, 30 Dec 2025 00:03:22 GMT  
		Size: 11.6 MB (11625089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24bf27c0bb0ed449a81b5fa6ada1e384d2e5ab45f9922c801299bb91e5dab52`  
		Last Modified: Tue, 30 Dec 2025 00:03:21 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e586810401da99692985a5491071e4faf2cbeba2c773b81a6c74603b1ef3e30d`  
		Last Modified: Tue, 30 Dec 2025 00:03:21 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fe4dcbbac465ccc98a30e7771909d8458a9f36baedec710f84603defa1dcba`  
		Last Modified: Tue, 30 Dec 2025 00:03:21 GMT  
		Size: 90.4 KB (90408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f519e2e0c5660ae6c3b23a247879ae3da45a30261b90d6a9e855c44ab69afa65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf20aec7ddfa5fede50a25e0ed3e08a788b1e122a1f045868785e829dd18b35`

```dockerfile
```

-	Layers:
	-	`sha256:5a0737d7a8f7467ed51fc907ab110086336b2a8248f44a46f1cf3e860d5b3651`  
		Last Modified: Tue, 30 Dec 2025 02:08:39 GMT  
		Size: 3.6 MB (3592069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba3fc4fd325b4e974cb70b4248875c0c5cd5f6d01a0aa49b27aeda7b7ea9fa01`  
		Last Modified: Tue, 30 Dec 2025 02:08:40 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7cb33f542c2b2416b8360d80bf270f017394a8248f5547bd25b910d362907e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60209869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d523ae26b69c0e69f59c722a906ef5e749bc1b0072a349d4b47e66752980ec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 00:03:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:03:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:03:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6ed83950a3f675536ad8634cde3cf4c241d5faea11ae3192ff5909f826256f2`  
		Last Modified: Mon, 29 Dec 2025 22:27:42 GMT  
		Size: 48.8 MB (48831993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2c77bf93408787969c8c3f6ff7213d99a7e697e69620cca332ac58446528bf`  
		Last Modified: Tue, 30 Dec 2025 00:03:43 GMT  
		Size: 11.3 MB (11283854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffa76c7561f8431bcf2d9458d0b5122c83188cb1a0af66ba63739670f119ad8`  
		Last Modified: Tue, 30 Dec 2025 00:03:42 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f90c9596551e2e36dca68165bdffea5d2e3885d8c814d8ec39b6430e18051a`  
		Last Modified: Tue, 30 Dec 2025 00:03:42 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8891a2507db7acd33db08d268da2d5cfe43517b88b3c5e4d64e7746d884a2120`  
		Last Modified: Tue, 30 Dec 2025 00:03:42 GMT  
		Size: 91.1 KB (91115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:677e960c2528d3f9423b79824ad6bd592c57b82a587b2e13c10fe717f1ced255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec4e91d533b3762f44007169dfd298ae15029e6c51d8049c5674a2410e24c89`

```dockerfile
```

-	Layers:
	-	`sha256:bbd84bbc74533abe8bf8740104e0d06c186ae3cff091c08be59b46b536a3e3ec`  
		Last Modified: Tue, 30 Dec 2025 02:08:44 GMT  
		Size: 3.6 MB (3592945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c39f6fcbfd1dc80794642dc576dfd48079c6de50372df3ff1ac44eef02c17cc3`  
		Last Modified: Tue, 30 Dec 2025 02:08:45 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:569f73a25eec4a3b557466945dda04a1ae1f934fc5a78c42ad8d638636122fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61823240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0141734533878f913b3560fcf901176219a5475150b8fc4bd7fec9b75d0b9671`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1766966400'
# Mon, 29 Dec 2025 23:49:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:49:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:49:58 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 29 Dec 2025 23:50:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a557815b7e39210fb0b4048ae58b1ffddbc8cf0f656a5974b6c3b24f7bdafed8`  
		Last Modified: Mon, 29 Dec 2025 22:25:28 GMT  
		Size: 50.0 MB (49955836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3de6d252031f63ff632fc93ea7483c181587ffd1f512b3291e0b985def1d502`  
		Last Modified: Mon, 29 Dec 2025 23:50:17 GMT  
		Size: 11.8 MB (11773710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca22956fa00058a06ab1e2099d072c71784938747e69eb7b2c33d6207f1b6a4d`  
		Last Modified: Mon, 29 Dec 2025 23:50:17 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7ceaa0da3811e5a3b3881ede84f7a7074693d4ba242f1ff4d4d5ea2d1ad244`  
		Last Modified: Mon, 29 Dec 2025 23:50:16 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7069b4ee28912050776dbcafefd634f2d18abe00ea821952ff474c4350422f`  
		Last Modified: Mon, 29 Dec 2025 23:50:16 GMT  
		Size: 90.8 KB (90788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ae12d6a98d6abc9394a195540135f308bd3b9ea1827fd6499827e5f5f6275bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc2d59443f1d23e48bde36a9a43f7471b46ce4389c27565186b7463dc9c4117`

```dockerfile
```

-	Layers:
	-	`sha256:4e3c76510133fdb29117515020b8e5d429ffa9c1f3936682f1c4402cb54319eb`  
		Last Modified: Tue, 30 Dec 2025 05:08:09 GMT  
		Size: 3.6 MB (3590022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55a4db6c529791e64f6a8846bb9fd757ab7637fc95ee2e67be2ae24de6377a40`  
		Last Modified: Tue, 30 Dec 2025 05:08:09 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json
