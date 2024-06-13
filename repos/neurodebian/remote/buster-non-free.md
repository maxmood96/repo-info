## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:701901ea9ba548d62c21b720af5083e6062499f31f108e36e68150ae3dca74af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d982fb8a9ff6ead7d630eb1e851c615db56c391e38b3708fc7887baa66cdd5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61071453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9ae61b9794f926d1a6ee3c26201d26654f555379ce1431812687a5628dc7bc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:82f06126089fd0ca482c29baeb90ef37ac3a9f5f6a0f2f5c968a605846627d47 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3892befd2c3f36ceb247ba7d906de12601d69b806597e65c4c837cf3d93df119`  
		Last Modified: Thu, 13 Jun 2024 01:26:34 GMT  
		Size: 50.7 MB (50657373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bcf4dbcb1a4bfd2a81858b9d0d83395974965a1abb6d86a818466b8bcc263e`  
		Last Modified: Thu, 13 Jun 2024 18:29:11 GMT  
		Size: 10.3 MB (10307535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8015ad836afea9b24bdf6e4d2d35c74ef6272ece2dbfadb9774ea1cb29d2acf3`  
		Last Modified: Thu, 13 Jun 2024 18:29:10 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b881f6ee9daf306c8cd344b4dc00f017523fadae7fe8f0de778dab6bf6c973`  
		Last Modified: Thu, 13 Jun 2024 18:29:10 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497302dd2576f598d67b7d31d9a422f1378812f40f898affd47d36d58d2ee2b1`  
		Last Modified: Thu, 13 Jun 2024 18:29:11 GMT  
		Size: 104.2 KB (104209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9f2707fd15ab253d9db738b3d975f5021efb2267fafc7a6916beebcac6f6f4`  
		Last Modified: Thu, 13 Jun 2024 18:29:12 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1b6c5b0d9b9620f4fc891599ce914cc388e35e049e932ff5777435eb833a88f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4230586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225831fed7c66b8f267999a4d1ffaad4ab6a50e76e1f1c6c26a2620fabad195c`

```dockerfile
```

-	Layers:
	-	`sha256:eb630ba519836ed0aa82819eb99ecec395929a7071daaa953373c58c36455aee`  
		Last Modified: Thu, 13 Jun 2024 18:29:11 GMT  
		Size: 4.2 MB (4215102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:152ab5892a0198a6f90c56d4066198b4bf3326f188ca2ddabbce43e600ca9b86`  
		Last Modified: Thu, 13 Jun 2024 18:29:10 GMT  
		Size: 15.5 KB (15484 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:buster-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:90042e51136c18b22f29bcde48518334d98b11d6f5e9ed074a739ad5e23e991d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59873044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fea009a5183136627105f96bf763f2edd3a34d9428abaf183d000e51db00c1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Thu, 13 Jun 2024 00:44:12 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b27aa5e3def1997c89f7bdc1f4e88d9b5b55f9828ac737b3c69360f3981256`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 10.3 MB (10313240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f3b0287bdf89ea74e53a548aabae1fe03c0146c47bf2c0dc275edc30feed8`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033ef7f47caf7b9ec62046617a97459accb5b59a7cc2e9fd7d3befc1d3ff35c2`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95a1bedd9437d691d7cf490e49ada31da729b4cc5bbff2f97af90bafbe84605`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 104.2 KB (104199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959acd77c1ea6c0d19eb80bf589e44188fd4b4429b9fbeac6d124c223bb0581`  
		Last Modified: Thu, 13 Jun 2024 19:35:32 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b2a9fc60bc625ab54f74b550029a9867810040fd46d61454972136511b5f5942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4231046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c920c3450da6d14de1aec48284e0caf2f54d90a8190e8f36c06cdf9a1bee59cc`

```dockerfile
```

-	Layers:
	-	`sha256:462ecbaecbe3703701a1f75f4677a588b94bf3f47ea9288d8b865b26b36061f7`  
		Last Modified: Thu, 13 Jun 2024 19:35:32 GMT  
		Size: 4.2 MB (4215284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e19e467a6a4c52fc701ad217d5e512ab94a2d12923fb2f130572f9f740dbf8`  
		Last Modified: Thu, 13 Jun 2024 19:35:31 GMT  
		Size: 15.8 KB (15762 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:buster-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:57f983e7f9f86acdfddb4d3f06279856dacc0db529dcdf3e7d9cfb75d9995c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62198803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8dd97f0a56db69579af7f6cb93a852bb53bc5231bd3d65066ca16225070f88`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e86b3dc0faa0645c9c93e23b272579368c4be6a1dfa842fdaa79acf07923271`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 10.7 MB (10672417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4763ff0412f0e24675a3c0094d231bb5d4e8e02027bf12f3b704a8d7af2450df`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d3a22329274128cc292bb8b17fbfa44e331807b81e2d773c7cb72f3eaa412d`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34750594939305441facfa5a6eefcd1cb932fb637d427e856e2d4fd8a40cb69`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 104.1 KB (104132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbb066394ae147de6d5ae62491985cfc67be643195f5d6cec344e2c6a9bfd20`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2c6a7a766039d129b00d2cb80d7d5d41439aaf354b23075d1e7326ce2f8c304c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1dc63b452c68125e8b1db6aac43ab686f120d7c6ac5815663e27bcdb864f93`

```dockerfile
```

-	Layers:
	-	`sha256:e2d563e3f4699cb1c3477375f76ac57e49733df27f30dc7ea01c8cbf4dd17229`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 4.2 MB (4212348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9c16586447c4ba568049064444e9027010f79435b5b909d83ee830c6561b3bb`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 15.5 KB (15457 bytes)  
		MIME: application/vnd.in-toto+json
