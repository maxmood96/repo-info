## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:92faf713ac5d573c61e929d1bb0885bd8206160ff2bd83ab782999cd95e11826
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:3614e7929c3729ee492900655cbb593213ff9b668b06a0a5b65af31ad4e250cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64956137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bb962de648b02471760878f9d9c5bceebfb355a0fa6460146e88b36ebf2c6f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3369c96af3a9fc3eb29426e581d97ea32eaab31c47f81ee9892accb3b232967`  
		Last Modified: Mon, 28 Apr 2025 22:08:32 GMT  
		Size: 11.1 MB (11105044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dd822d9757e8e19577e208ca25031ec40df49dfbe8dd27f79473b2eda7f2a2`  
		Last Modified: Mon, 28 Apr 2025 22:08:31 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6efc71d615d74c4ba039b2798948093b14e30d977f385680cd8c9bfdfe2099`  
		Last Modified: Mon, 28 Apr 2025 22:08:31 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9f32be21c243ea5db70432799ed926d4f88873b7799935404984d527f84c3b`  
		Last Modified: Mon, 28 Apr 2025 22:08:31 GMT  
		Size: 101.2 KB (101195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:051cbd07a47217a799ca9328cecd294167f18ef76f98afdfe7a7d1e58062f95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8d47fcea2aa238b119b230d048286daf2dbc0c4874f79b98bea4b44dec0b7d`

```dockerfile
```

-	Layers:
	-	`sha256:e7515c8ebe3afb7d5465b050016327ae00b50e6620eeffc63b538820def8f034`  
		Last Modified: Mon, 28 Apr 2025 22:08:32 GMT  
		Size: 4.2 MB (4234764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d532788aa376107485ef5e11dfed5d64f23507c398c86d35c0f454acc6f12317`  
		Last Modified: Mon, 28 Apr 2025 22:08:31 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:54cc18c5f8099aff6ea8ba3c72a11e79b7905973f6217160e4926034ce9350a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0171329c6886636ba22a3b2b035e468fd6d0f8c2bea8dd80523efc98efcf258`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9753e330284da1899fd231bf33fe62c0d83e3f17a233f3f30f504bbb6fda21`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 11.1 MB (11106062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4499b0e25845d2e35fdde74226cf5901ec7e9be9382eed98b9a3eb02064d539`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4039d5ee1ad977691de6bac1fb9373ed9749a1f33ec81bd570216e56c21b379`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ea557c3b7e8fb6dd8d91d49cae4f0e43f2c39dcfedf77ad960408c3552376f`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 101.1 KB (101116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5043ae029131864ae3a944a2a752566e6db3aa2a287e8abf3e0f646a0231fe27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92230a230aef69834f4829c9064c575d06f45e0dc635672186d1e3b544444f59`

```dockerfile
```

-	Layers:
	-	`sha256:1c760e8eb6dee853f27cb14705ec5ac2b466a26636ecdfc31f9ecc865866d939`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 4.2 MB (4234371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5319aba817327886dc313845a89cbd8ba1eaa6cef5c0c9fca089e56606a8099e`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:ece69efe387772ae71e49334ad14fb71fca34e8398e9eebc4945eb2e5b5896ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66286721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b61cac2b83d8e5742e4d51cc760dc2ab27575c2116e7a38396a5560908485ae`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Mon, 28 Apr 2025 21:08:10 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baa54ab7aadb65f6ea817faeccad8b1e8490b283148d13620fe04aa91bcc5a2`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 11.5 MB (11500361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617112d89002a29be31993a712480ac76d7c3fbdcb5c6f3cf40b5b4b8fa886fb`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8d4f800552b99deaca99f39e9c946843f3fbc3a4547f43b1583fa99c0ea721`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6fbe1de2e956cf97516f96ef1b5550fc3c0fd3e6ed042f2bfafdc5860b98e1`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 101.1 KB (101099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2b4b8e1705c550b0dc744d427ad3d78c1e2c71de91c2c660f37d57a1ed1f3bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7032562fd624591c59b125344aa2165980d603d957844a2ba94775a0137f3066`

```dockerfile
```

-	Layers:
	-	`sha256:d589af26589c547278945a991c581d65bc5e099cf7a2e6f20c7f76b26303ecd7`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 4.2 MB (4231226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c76920d86db0de668b94e501ce99edc5079abcced341354afc9d97bc2c02b104`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json
