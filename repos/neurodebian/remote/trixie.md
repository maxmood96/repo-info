## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:87693cfb664c3983f3e574e1dcd5b58f82fd2618b8af3a364767508759c8e2c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie` - linux; amd64

```console
$ docker pull neurodebian@sha256:5445400c594afd56d8608d270c0e840a5bdc8ce8eed14c50875b111ece8c8967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59667200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1692c2ad0959aff9134072de309c7092e4303f34bd66175926b4536f01737b1b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf661b2ff63805151437f18c9fddf545dc18823488c0dbe851eafeba8066d82`  
		Last Modified: Wed, 01 Oct 2025 00:26:33 GMT  
		Size: 10.3 MB (10289495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030c7393f1d0600f3d5801fa9a09be77c972b3bf6cec3d9a0ceee41e16f80f79`  
		Last Modified: Tue, 30 Sep 2025 01:05:19 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7679f2a094fcaa509ff0dbff39c2f33e8f9ee67eba015e63ec580599369bd963`  
		Last Modified: Tue, 30 Sep 2025 01:05:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fdaff3323992c80159a90ce241b8c1e2eecfc50b87e4e1f570519c04063c53`  
		Last Modified: Tue, 30 Sep 2025 01:05:19 GMT  
		Size: 90.2 KB (90176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:11379453b3c698293768b9d690e1a7e9d3b6991a688f6f2c6c9d46d25b7a1999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e291424f296bf0582d068b79c4a19e3cf1f75fa0e7f7d4051e57733efe754ae`

```dockerfile
```

-	Layers:
	-	`sha256:a5d6e8b4a14ee685087c48f425191d4046aecfdc2e2dce91edd6ba320a8a65b9`  
		Last Modified: Tue, 30 Sep 2025 22:08:37 GMT  
		Size: 3.6 MB (3612981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba41c16a9c24d09b71598c74915dea63db262a1a93abcbc3f0d247b9b4c11c2`  
		Last Modified: Tue, 30 Sep 2025 22:08:38 GMT  
		Size: 14.3 KB (14294 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5d39e0ae09097ede0b7dcd605763843cc32f5d004f39cefe691f3534fcabf107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59815441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d12c54dcf7bbe6d3551a1d49ac956e0b9ef7c361391bd2511992d7c2ba5cc6f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6f6da96540c9f6cf298b7b364c63b1cf0c3929b805fed831b6c1c3eae4d87`  
		Last Modified: Tue, 30 Sep 2025 00:19:26 GMT  
		Size: 10.1 MB (10072980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a478dfca60a2c33636ca722a574ff603abd3fae381c95be0c7bf68323a3704`  
		Last Modified: Tue, 30 Sep 2025 00:19:27 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5474e962acd88276c7b9fa402cc148afe511eddb2832d559ea63b51fb720b0a`  
		Last Modified: Tue, 30 Sep 2025 00:19:28 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094906ccc10fa032c3efb4b206bda6edbedb9eca7903daa2ebdf676a5f615361`  
		Last Modified: Tue, 30 Sep 2025 00:19:28 GMT  
		Size: 90.9 KB (90866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2be449b53fb3b4125c74bfaf49a273c82589056f7a7b58ced28d693d35ecfd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf5e15992d5473686642c610909b239be7d6cf3f13bcfccc273a3f7cd5cd553`

```dockerfile
```

-	Layers:
	-	`sha256:ea9f419913ead7a4c0e010568c2d3864423e07529314b03a43cadf13070d7ebe`  
		Last Modified: Tue, 30 Sep 2025 13:07:45 GMT  
		Size: 3.6 MB (3614508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e6d045cefb6337ce69dbe9c61d5d154f22a2ddc355e21d8fb66a2d9f615939`  
		Last Modified: Tue, 30 Sep 2025 13:07:46 GMT  
		Size: 14.4 KB (14431 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:8a46319c2bee6856b4f764ac30025c5587a5ee243fb31b30dbfc8d7fdbaa6d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61356323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e989f30d27cafca9de5bdca46f6e0f4139c1fd7362a134d113c77557fab4dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f1c1f592b5569b5e2093c3107a48f2929b609f05af6d24c06d41a7ec1ae5e0e1`  
		Last Modified: Mon, 29 Sep 2025 23:35:36 GMT  
		Size: 50.8 MB (50800229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ab973589bc45010616b19754c3c69e0ae9f8ca8970197b3299d394ea33f588`  
		Last Modified: Tue, 30 Sep 2025 00:23:16 GMT  
		Size: 10.5 MB (10462616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efbe96c0b7cb9c8886f791f5343077fbcb6ee8bf991286ebe52cab58d6cc892`  
		Last Modified: Tue, 30 Sep 2025 00:23:04 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dea642e4992382c23719b878885f48c32247f1f5867d347ad4c22d63c0a8720`  
		Last Modified: Tue, 30 Sep 2025 00:23:04 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6ae40746c8c652627ef29267be656c50aab350b775d26b475917c7e2742ed1`  
		Last Modified: Tue, 30 Sep 2025 00:23:04 GMT  
		Size: 90.6 KB (90577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:01edb6d5394be68b0049fb213c5711380de11bbe71bb915c1a99290309011366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7b3eabd530054c8c1027eb5ff3de1c92acd70f4dac5652e04a574e629a340c`

```dockerfile
```

-	Layers:
	-	`sha256:031421d4527aa62b75263e52be1877d3065aa1b9c5575c49b0f1fb55f48c5bf5`  
		Last Modified: Tue, 30 Sep 2025 16:08:34 GMT  
		Size: 3.6 MB (3610930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c15ca298c4f9b159a9a1e17f17ba6bf440488c13b2b3af4a01a92335f30ff50b`  
		Last Modified: Tue, 30 Sep 2025 16:08:34 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
