## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:b0d72ead4f7914db488f7779d5259a33d59b18a4f3973e2e889ebfcd98ad66fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:195f8e982bb7f7edb9c996c204b1ddf8f55e2f2fd4af59a61a1da42b7f4f3ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59684333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0475b85ed0252659214671d27199f0988e3fbf8dcfdef45481ebb51adb66f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0958f60c5152275d8e2aa46f27c31bf8e62350466d9254ce5ebe1ff17628eb`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 10.3 MB (10293014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a99dd4cc6b98f202f039fad4aabf18786db50c45be9db53232d5231a40f590`  
		Last Modified: Mon, 16 Mar 2026 22:45:01 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4737476d54fc963844a726785647ae72e1ac4aee6752b7e79082232ad05deb19`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2682215c226f042ddd3cedea53ea769510c93b14f86b5dd01d531458742684b3`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 90.4 KB (90442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac85d07e7667fee3e1471587f9fd0b61f01b282f168d4c4935268613605f02ae`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:adcaa56d48f63f87e006d4314901e4a85e4f42f6cc57143d1847c015f4916be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c092da940be19a97a6f0d4f93e874c6efd7e0dd855d2955a4ed5636f3f7e343`

```dockerfile
```

-	Layers:
	-	`sha256:9b09648a89fd35b6d25c36f95b0b983326ab1d1930c696db1bd18f2e60f2c3cc`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 3.6 MB (3614144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90f36eac91ebd943a10f26dfffcfb64cf469ec6201994405a3e0632e43fe279f`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2c289b0c2d4bb5631d73f7167cdf0b1469136d430775c9e499ed655b2e227727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59837297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99544e8d595bd4f4f730270ed8507040f7e5e54d1d5907a98249a0fa865c709`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:46:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f92c8ab9372506e674a894d9fd986fa8e5e967b72d2112de3a10396d44ded2`  
		Last Modified: Mon, 16 Mar 2026 22:47:00 GMT  
		Size: 10.1 MB (10077962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca2e88d525000038257bce1b7337532919c6947404971f468600b39f1dcb676`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b7f8b4c55645ce191bd8e488c7f43b133f1a9012d1ff286ecca0bce803b557`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab02f003018b654c743fdaa120b30684485effd2a5de4335f24daa16b043e87`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 91.0 KB (91036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c50fefc97e01b6c27dda2c96f787d121d2cf01e76a012c884dafded607d742`  
		Last Modified: Mon, 16 Mar 2026 22:47:00 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a9654212e73c8868169d367045704307ebf7b85f4c6d53917c6eea4945a6d206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf23371fdc78a81a3ee7507687a8bef9056a048d09049dd4392d262edc0112a`

```dockerfile
```

-	Layers:
	-	`sha256:01736020557ccdc3e3407249cd21e0e8a96572884941062bec8e07bb210eb8f8`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42579bddc23e952958f660dcb8a9bf19c229da06cef28fe92a1fd1d0b7690521`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:98100e9cec7a59df1753099be2a8adc41c8d0660b1e6c420961f7587698eb00a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61379923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c789d63431eab185cd52bf6789b84bf1fc1859e61ecc43ab80d6cdd0d5a39f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37abea767e6bb8c916daf978fb4a1dac54edacd3f804121916ad31dd00d0955`  
		Last Modified: Mon, 16 Mar 2026 22:45:11 GMT  
		Size: 10.5 MB (10467046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec540dbcaed9de978c5cb39191036757c8635984927ea8201c71f777e2cd422b`  
		Last Modified: Mon, 16 Mar 2026 22:45:10 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6bfb517ef690ae62f0dcb8ad9abfac9e83f354ec0fe4508a61113f68f494bf`  
		Last Modified: Mon, 16 Mar 2026 22:45:10 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4ed0cf4df19dedb0d14f9750f7cb7af25c17968a684c3068a6834805d289b0`  
		Last Modified: Mon, 16 Mar 2026 22:45:10 GMT  
		Size: 90.7 KB (90734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408ea60a0fb71dbeb5a18ead26daccafc96826a72bdcd39f8e4bd6a6d0b7c74f`  
		Last Modified: Mon, 16 Mar 2026 22:45:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c0e9bc43f78cd1cf795cc271385fea29a4f11fd54e905046c1fc5d3eb7ecc405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ca8c9009e4ae9378709fec75e4d6a18915c9072e085f61de88f8ac31f73595`

```dockerfile
```

-	Layers:
	-	`sha256:16f37269439e4540d7453667eb75ff80f7e1dd937d18e3a35dcddd7ba9418f97`  
		Last Modified: Mon, 16 Mar 2026 22:45:11 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffd1eccebc7118d1a1fd1ad1dac6b36ed9ff3bd241e89034ea71a23a9e7a3d7f`  
		Last Modified: Mon, 16 Mar 2026 22:45:10 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
