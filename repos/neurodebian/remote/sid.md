## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:cfbe31e8f8216a29bec1d84ffe30e9154e7006818f7e0fe5af624b8073a5e896
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:722b3734a074f52b537930b8d13d96a90c23904dea0de135834085857118a3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60161613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9e6e7067e1ace693bcb1daa4cb49007ce4c30aba88f93332e4d3297eef23fe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 00:33:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2e77f12282fcde2c6f54d54624e8a7eef59205bf9001d755b40c1e76ea8e3238`  
		Last Modified: Tue, 04 Nov 2025 00:13:00 GMT  
		Size: 48.5 MB (48485640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a5b96440cbeeb7769517ff329ed0883771f1e3a99f7933b2173145cc5480cc`  
		Last Modified: Tue, 04 Nov 2025 00:34:04 GMT  
		Size: 11.6 MB (11583255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4375310c6ed16655ad67365cd813771aabbbe8573c45b873213c2074e78f4528`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f426f31085761e6a46465387404baada1a21b1249625e208e4bf18e8596c6d`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e900ba29d98519727c17183e473955bf493815c7da5e3103020a8176f31fc356`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 89.8 KB (89813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e4a85c3da567c9a45c5c7f1618d5098c8ee258bf7ea9c83695d83dcd6a8f4c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c45e24afa3b99e6ff745dcae8421698af0fa6919177fa5959f32b08970e1c16`

```dockerfile
```

-	Layers:
	-	`sha256:45cac87f230eb98aa986ff794a77ff43a15a3bc71644de748398a4360351376f`  
		Last Modified: Tue, 04 Nov 2025 11:08:52 GMT  
		Size: 3.6 MB (3577395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c589fd0990d047638dae2719c765f5e3f9f00abad8733ec51451217ce909976`  
		Last Modified: Tue, 04 Nov 2025 11:08:53 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c7cce04f019cdaad0ced550dca9af4ce069da69a580048487ac8e45f4dfad4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59938487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792e7d0dd2ec4ae27f7d32f4408e7344a709b1185f2c60131cba267efb2d3fe0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:32:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e6429e9e41ca9e14d8856af7a396ce50bc2b9896b4f4cd83c36fd480cd4514de`  
		Last Modified: Tue, 04 Nov 2025 00:13:31 GMT  
		Size: 48.6 MB (48586018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e357ec5b83e5625b9f94d5fc603d2031b8514071e4bd32938375326d1cc6c9d9`  
		Last Modified: Tue, 04 Nov 2025 01:33:04 GMT  
		Size: 11.3 MB (11259052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d225e2c5c4d55a1eeedd7d833cce1246eb8fa46211165fba4866d1f770d13666`  
		Last Modified: Tue, 04 Nov 2025 01:33:03 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d0a3c87f92b126ad11f68b5e3d11fc24562344b0b4d492241f33509c2acf11`  
		Last Modified: Tue, 04 Nov 2025 01:33:03 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f467de9381fac753e2f32ec130c3fdc5bd52c38944cf43855a312828900bb2`  
		Last Modified: Tue, 04 Nov 2025 01:33:03 GMT  
		Size: 90.5 KB (90516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b5a2152fc41ed9eea92688f57fddcb38f01656a94abf50490022d188d6e5d609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69957ad7a64f6286d83d10828ce2f0c30cc145aff8c0291731392884594992a`

```dockerfile
```

-	Layers:
	-	`sha256:5df592788eddb75c428d5fba029ca483e1a5adc0e0e03f142b8455a9f3235ce5`  
		Last Modified: Tue, 04 Nov 2025 11:08:58 GMT  
		Size: 3.6 MB (3578271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fc7a61a4a383f5b356e7bb4721d7e94c544d6ea8839c32df57b0b84c4e15cf6`  
		Last Modified: Tue, 04 Nov 2025 11:08:58 GMT  
		Size: 14.0 KB (14028 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:9b677e080c119eb4a17717438cd0c8483c91f4ea704a02c34b6f6506c58b0ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61636868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4883a56e806041e69ea01712a928a707f955a2916bc0a6ddf0f9111af750ddf9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:38:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:37a822686dc57d9a439e8fe6f90a9020bbd58f684341d3cac6e3e13c68f3344e`  
		Last Modified: Tue, 04 Nov 2025 00:13:36 GMT  
		Size: 49.8 MB (49809007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3095763312556ed24fdf8414a87f3df47e55ade17984072746abeb95af700d7`  
		Last Modified: Tue, 04 Nov 2025 01:39:06 GMT  
		Size: 11.7 MB (11734751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20daa1451a1c5e4864905084a53cb50a8ea4ecc7152fe1f07eec291ef587bedc`  
		Last Modified: Tue, 04 Nov 2025 01:39:05 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a436f1558d69b26b0f120fbf5cb58bc87b6656499820ecab74b4cfba29a4f5`  
		Last Modified: Tue, 04 Nov 2025 01:39:05 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d31efbac8a3de9856fb31500c282ed7ac97967a0bfb99748f45785bf8ff335`  
		Last Modified: Tue, 04 Nov 2025 01:39:05 GMT  
		Size: 90.2 KB (90206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d42fe0312df5575f7895f36d60444890b9d1945492b4ebf532dd5fe409a8b2d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8feb1ed938280b209b67281e45960fad0d7b9e3883af43573db10eb3d7a4438c`

```dockerfile
```

-	Layers:
	-	`sha256:c8c06839190cbb474a9a1105dae3eba7bf063e0ec0058bdb7f336eb8fa3fbb48`  
		Last Modified: Tue, 04 Nov 2025 11:09:02 GMT  
		Size: 3.6 MB (3575358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a58ee565df700715f4dc6eb2260eab6c98353f3ffcaa0425fa571731b9f3a9a5`  
		Last Modified: Tue, 04 Nov 2025 11:09:03 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json
