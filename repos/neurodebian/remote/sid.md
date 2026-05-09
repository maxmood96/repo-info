## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:5462c83858d3feb66eab9b4197a35e7c3f2c97168a1f033fa5ff54bc7b0089db
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
$ docker pull neurodebian@sha256:8a4c8e5c02d9c032eff3aca30a89bb11dd0afdb58ba10ea078d0248b1842a7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60186278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6739630cd28c1d946604021f5e65b72c0489c653c44c1558e0271fc06dc041df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:44:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:099d3355eff9ccff1f5ee3b288e1ead2e7035e89d68d0fc80f60a9bd7a9815e3`  
		Last Modified: Fri, 08 May 2026 18:23:36 GMT  
		Size: 48.7 MB (48702238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e478533e6ae193c6fcaae041855399f59338878fa7e4644c40a17730309dca`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 11.4 MB (11391655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601904e49e5900acca267146a686c3f2a2a62c1246a1e38d212fea83bffbe0bb`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d949441ff174a57a6fc707bc732ca1634e6558df38f4715cbfcbaebe99f00`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dbdaf7f7809f135ace320cd033d9a6d661f149877bfc78ee99f12ba8f0ae08`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 89.5 KB (89483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:412cbed693a82d055a8f5357999ea9f0053401665d64aeef08fd5f06d2dcec0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66b334229b8a964cc51e6b877024313d7cc9a4d9a13c5c0ac570a1714ad128f`

```dockerfile
```

-	Layers:
	-	`sha256:2798dfba3ee312a5c3c86f73e2dd22eff329c06e0ea7cf6108e8ab3f170b1791`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 3.6 MB (3556234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c8c7bd53e080388c9a1eb264e0fbea45b097b66db0192338955fa9903db445`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 13.9 KB (13903 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8d042e0c6b2b0bdc7bd6088a54197a0062b4e77fef4e334f0b514b42ce76bf43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59920057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca4e48d28afe7d23765196f54fdea60741801af0f6b198d4f1d7aff164ec43b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:46:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99699fbc842c790e8471e4039d9c409499f27c659ef9c4d3336a0743660ec819`  
		Last Modified: Fri, 08 May 2026 18:26:06 GMT  
		Size: 48.7 MB (48734151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2a6841249cc037385aca9cb88bc26e07cfa8ed2a3f883ffdea8ae1be354b5a`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 11.1 MB (11092978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0938906dfc842f7becc351af1835f05072b61776a354569f75a22d1f1e6ac299`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0668f71f67e7f7a552b9af4850f0941fb6afd56c29cadc4acd358584bd8a7518`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c06c9c91f639614d4952e3ed20b59bf97c833709c3620987f812909d74f82f`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 90.0 KB (90027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1515e7f8ac45bd3a4a536ba87d58574f9beedb409c59fc72752b88164c944056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36672cedf692ab9b354876cbf435214d90917c05080107060f25e608acf9f045`

```dockerfile
```

-	Layers:
	-	`sha256:1aa37ce6e70e12258b02b458c1845581d86ecdd450c40a6a59c724b75463cf93`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 3.6 MB (3560939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da2b316ca48ed77a2b1aa0ced2f3d8e67b58143d8135f7f24e5168d05f49127`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:73ba3061222d6c325c0a346e63bc504de41f9532e07a59209fa44e4519dcdabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61725184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5af2eace4327f02703f432d25d547b430da3ef4030f8154d0d4dd1322459e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:673cf326009083501c3fabdd17567c937b894deb57d94461178ef18820adb917`  
		Last Modified: Fri, 08 May 2026 18:32:00 GMT  
		Size: 50.0 MB (50006715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f0c0878f24a22f4bae1cce2bb33ade2528e750968c7f19e4683f865ecf624f`  
		Last Modified: Fri, 08 May 2026 19:45:28 GMT  
		Size: 11.6 MB (11625846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83aff980bc85ff5b2ce155faf54e6e3fbf0412fad6b9b461726d7a94f49ec8b`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1690741b56c00af9a9e027b2f45da2d3c964439f6016d2a01ae49e540c9a138`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403996057114e2cd0d36ee941960ee517faaab068e8e0cbc9de09e96c9223a56`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 89.7 KB (89717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ab1c10a7c00e20030be43916af676fbd69ea524a13a3d1f1100bc9cad07f30b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df6d819178bee19b394bd34bd99b9a33ff2d758ed51a85705d80ba78362451f`

```dockerfile
```

-	Layers:
	-	`sha256:2890089b6f33dd50ea7d84ff7f43fd03e40b52a12e2925bb4cd5456bc7dd9b0a`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 3.6 MB (3554180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27aea920f78950a42d40670e7327c30443ef99b9d23d92570dbbee1e83f95701`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json
