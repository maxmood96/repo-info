## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:00d9d0aaed676bf574f21aefd9fcadf86ebbf0a63d75d29ee4b5aedd08795162
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ad0cc82f64ed565c7c2869c4526fe7e186ea4fc902a699f42dcf968f5e945db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66307365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03688bc896f6ddd4f8b0e35cc44e9c9f1f106a8631664181920f8de8dae1aa37`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda956ed2e59dd498f275947a4d52e044d1904ec6f658f010027bb8ce875371e`  
		Last Modified: Thu, 13 Jun 2024 18:29:02 GMT  
		Size: 11.1 MB (11105053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b160adc8af3447541489d08e32ad41cf072d087ba6df01b14bac6aa48dc1528a`  
		Last Modified: Thu, 13 Jun 2024 18:29:02 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c63b1c6b51fc0bdb1af4c1794342a43c2b7ea8fa5970420122c9d539815268`  
		Last Modified: Thu, 13 Jun 2024 18:29:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dfef3a713e52434bdef1a7e48fb370ff6ff3959cfe75ee08bef455e5aa6c05`  
		Last Modified: Thu, 13 Jun 2024 18:29:02 GMT  
		Size: 100.8 KB (100772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84861e4a14d452b900523c7ea04e2ae9cbdc051a6e5fdebbba82e451a7c28eb9`  
		Last Modified: Thu, 13 Jun 2024 18:29:03 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fe9b93f916d8107adce38533b39652b78f344ec091505566c97a4a7bf607bf12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4214906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a2d0a6ef07f3c2e99d2d835dc1917a5d35d9092e58e800eb0bb6467d8c5562`

```dockerfile
```

-	Layers:
	-	`sha256:fd65ce0b0bc29451b1d39a3a57717b95c313c828a82af8c114511f558c284298`  
		Last Modified: Thu, 13 Jun 2024 18:29:02 GMT  
		Size: 4.2 MB (4199082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7562f64b448561700ba0dbc9dadd2fc7958bdc9bdc9aae95d38d7a0e715536e4`  
		Last Modified: Thu, 13 Jun 2024 18:29:02 GMT  
		Size: 15.8 KB (15824 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f1e392da199b8dcca45f896a5cab373811b3aa702e8615419c65ddd7edfc74e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64948463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168acf79e5122f2c5e8a5c166e82192cf5852ec99f928fe129b530b1d79bf4b7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ef66b54f3529cd7df198490a60a02b9a4e099ea4456cbc230affa6271d7be`  
		Last Modified: Thu, 13 Jun 2024 19:36:08 GMT  
		Size: 11.1 MB (11105804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf9da50bd694d2938f66745014033d7f272e00c04af58b00384767df0a68779`  
		Last Modified: Thu, 13 Jun 2024 19:36:07 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d1d085e2488d140f07257a03441112598facbad0671d3f6d3aca4474943da`  
		Last Modified: Thu, 13 Jun 2024 19:36:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a6ba47d152985a5fc3c5a383c539496f19f49199c0ba685819566962b387f7`  
		Last Modified: Thu, 13 Jun 2024 19:36:07 GMT  
		Size: 100.7 KB (100727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea6100cf3e072ab362a57fe12dc0cbf09696721e80557e4b9e225c44b3cbfab`  
		Last Modified: Thu, 13 Jun 2024 19:36:26 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4da3bf242d095595bc989ae17d7609c596a0b91092deabe0e5f44a7226f92d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4214815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46662291b74b853620eac37118bd091db3450215860660763a774ef3e6c7a948`

```dockerfile
```

-	Layers:
	-	`sha256:bd2e2a297ec21ebdd927953ab988ea32549b9e3e2b03857c070c868ad1929315`  
		Last Modified: Thu, 13 Jun 2024 19:36:27 GMT  
		Size: 4.2 MB (4198699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5f5aa795607d3ec33b9bbf4089b270c6af4bdd97c4778667c84578e7db6c552`  
		Last Modified: Thu, 13 Jun 2024 19:36:26 GMT  
		Size: 16.1 KB (16116 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:30c029632c96bf37af9b76eb0393927bcf408d4d4637bddf613a7594b2681b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5864c6def933a6b6dd9adfb7a5ec63fd1f46aed4cd44d9bfd0cbe3d67f45c8c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b13addd2b2a32b9d1ff2ea9286439b5540ef92b6f2a15ae59e20801eaeb8115`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 11.5 MB (11500167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925784d52a7a52e17776422204b33b6f319d5ac291eecaed873d7c75d0bf7b5e`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc25404734dead4fcf99099c0b8c4c255e177881c3cf9e4bd15eecdda5bbfeb`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77175288a751964832d472ca502af30d298ab6d18b500e39100c7e2cf1941a1e`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 100.7 KB (100656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e403eee5dd3ac973d264d6caf142749476a40597c843100f860fd812bbdd7152`  
		Last Modified: Thu, 13 Jun 2024 01:59:16 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:20b1a751fa916af4b95b9306d65f00cc6ede2b46bebc04dd23cc8fd44391f864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4211329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9bf79df5b568b2fef0e797dc3f58e562b7992622978ab8ae0de582edd25ac64`

```dockerfile
```

-	Layers:
	-	`sha256:5b95beda90bc46a2b778e530d4afd832492d8e6d2ba670872dd2bd272173e02f`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 4.2 MB (4195537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b42daf680929d419028ac29504c6aa3762fea17ac4478e351fac146d840b2c94`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json
