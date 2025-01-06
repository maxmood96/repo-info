## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:e7c0d77acdd38391058bb428da4b25ac4b5d5b17dbc921ee7afb854783a1cc48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:9cdfe6f90f096c5886af048cddf57f84f7131abc4faa5f65638d66c77660e090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58544425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29dae39f0e2a61e2773abfc9d19efaff6e24355ae35e8f376529d52c260d4529`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114eb8c7559544e979c7bc06d71d09eaa2cd00debd8cf4f03a56d8104b7699b3`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 6.3 MB (6308996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff80e11993394c1dc9aaa17af36dfa33cca39fa8e0caabe1b3bf52e80a34369c`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4eb1dc4c12753dfe02a45cea97e094916913c37268158aa3b340700e68143f`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12f43e28b0e223dee7e963ea7a4ad3a48f843457e481ee84cfb74772191cd9`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 91.4 KB (91443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405db61dc15551d8850b73eec4f6ecee2d15504c5d277afd2c8128e17ecf6611`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1bf2d8e93155ae981f2f562f22bf9918fdb877c66cffd35655fec1d9b1f39938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffd90ef4d3ae1ed5361af576f9d3f2c0d2a5754f07e470e32f3a78bc8bd6096`

```dockerfile
```

-	Layers:
	-	`sha256:9702d640d901ef7903e74e7c2b43af913d4f418a939adc866950dcedaf2a783a`  
		Size: 3.6 MB (3559130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7bb223c6e89608e9722bf8101c7626ae5724ae67e6be3bab333911378929ca4`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 15.7 KB (15653 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c7ac4ef4afbf39509f7a22b31591f646ef72bc02b766b53e5fd512cdd67e0175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58746750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bed54a230a0fd8bfde46f98be15f4d3b97ce2d877b842da7ab902c830cee5c0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1944b6bf321c80bca628a1f2806106275b5823b1d9a2194d80db72c1240d0`  
		Last Modified: Tue, 03 Dec 2024 06:18:20 GMT  
		Size: 6.3 MB (6288605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f848cf5ceeefd58f0b25aad8a4ae18f3778a65f33fc9460661f7b5f4b7e340e`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f54f177bb5980856b76068107daf64a196986c4cab67e6faf6eaf3ed6dda566`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410851795a0d0599053b940c07c6a163f0727fc402dd559169c25bd9de9ec7eb`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c880850a32196b5042f578dfb72c4fa93d1ee7ebd60d71fa4d5fbe19814c1ac`  
		Last Modified: Tue, 03 Dec 2024 06:18:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:22661e3cbf436b44b80103996ca2bd6577e74d6b1b8bebb5202171aadd46a284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d846bb8b6f1144a2d45721e8f45c30c3f32192c7a1ac72ca6b7268efa446fe48`

```dockerfile
```

-	Layers:
	-	`sha256:96771062d69621936e46943c2483b9fbc12aa2771b6c3722cb1035b36ef91682`  
		Size: 3.6 MB (3564009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62c24f5aff628042c5046d45e533873a264167660d2769d5c6aa4aad04528fe9`  
		Last Modified: Tue, 03 Dec 2024 06:18:31 GMT  
		Size: 15.8 KB (15793 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a7f28e60fef8ae8c66fd2dba17b3f842cc070ff0f190ebc2bdf9a7a8be76fe7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59703410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a1f70a2c0871c021a308aded3c9b948de0de66faaa7121a2d269e4640fc96`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998bde38fb7afd531148bc5ada8932ba6909774db1014c810250d2fed9705c28`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 6.6 MB (6635982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff379f8e9bb8d25d6e0f0189f738f8b022e1073b791de493bf8117cc6d281ae`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863c1b51d89e4dd4797ba1c7a7da71a5c460240254b1e7853212c5b2e920c1af`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bc6338d9947bdf727b4f355b78ec884ccc098bacc03deb3d7965d5d04398bb`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 91.6 KB (91629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deb6e8c73557a116710e67686758ffb933b5075a0bed69a3dae3ca0be59627d`  
		Last Modified: Tue, 03 Dec 2024 02:28:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:74f05ff960ca0068515281f926b0c25dbcf76375b4f99e58125b16a689b862ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d55b24693960716604398d554cbad7c385b5f86da205d5292975eeb67833ff`

```dockerfile
```

-	Layers:
	-	`sha256:74ca85f2e86db85f7b30f20d46e8e42be283a7b27e1b60976e0ff56e761fd5f2`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 3.6 MB (3556371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d03ff36e1583fd5288b7e43255d4ae49d2af7984f1801d3d5ea02eae17b0cc6`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json
