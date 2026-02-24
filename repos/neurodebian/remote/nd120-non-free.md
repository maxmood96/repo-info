## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:6c8e09ee35c28a4fb10bd1452becb3d66051a4d0aa2a95c8a49e6247f32c59fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d6fed7c35647950f19e744d0cca167e1bbfdd94181873ffea570fbd709552860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59858011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137ed41bb7ebfa34d824a3747ed978ea8b1ce0bdc68b7c2c3db4bbcb4c05982d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:26:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:26:27 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:26:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:30 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a5b77fb71287fbddc5b2dda711188426905c523cdcdd2b776c294c7616213`  
		Last Modified: Tue, 24 Feb 2026 19:26:38 GMT  
		Size: 11.3 MB (11273218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bd161888ac7c12049956e9a2f0a1da017c65888837c1a7d6faaad4030e800f`  
		Last Modified: Tue, 24 Feb 2026 19:26:37 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134e88d272058c211a2b335d90edb18be79c78e4ca2c1fb760eccc8f301e9e33`  
		Last Modified: Tue, 24 Feb 2026 19:26:37 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d045a77473fbcaea1fb392a59ce3daffbc40197a063b36b7fb36aaa2a32dae0`  
		Last Modified: Tue, 24 Feb 2026 19:26:37 GMT  
		Size: 93.4 KB (93393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0204ca98d7e2d1b2ca285e28c49008eb99a810a5e90ff6cf1038957835d256e5`  
		Last Modified: Tue, 24 Feb 2026 19:26:38 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c3d7513e21540bb95546aaaddacde3db8484b73ed65c48659cf70cb400f757ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86589c5929bf4660a77c84d1a907e95c799642c1b9ad818937212e9fcc861ff`

```dockerfile
```

-	Layers:
	-	`sha256:c333fe6713f88d9ce5d5751993395c690a3fdf3b89fe82cd36c1cda5085d7471`  
		Last Modified: Tue, 24 Feb 2026 19:26:37 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b9749786a0f74957387234e9965f8cfb53450af990e01a0902e75e96172149`  
		Last Modified: Tue, 24 Feb 2026 19:26:37 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:385672b15652221d1e3dbcc0f514e3c5f816175706a10df0dbbe13dacc1ffa6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e740bf18441967b381cb4078c9baffb30efcb5890a7375c79534715faaab5f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:31:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:31:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:31:14 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:31:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:31:17 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb20c79e9a4adb290de38c4b2e32725a39d70d288f92b3b09206b91b23fcf59`  
		Last Modified: Tue, 24 Feb 2026 19:31:25 GMT  
		Size: 11.3 MB (11252993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9146f69ee25106214f9633778dcc32cddf46e76b78c0d979ede79c4c31285fe`  
		Last Modified: Tue, 24 Feb 2026 19:31:25 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47fa5edecd0cf490312a0af95fb264825c18cfd67f7fd8c3bd62bc3a265cb90`  
		Last Modified: Tue, 24 Feb 2026 19:31:24 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4967e7c08b2a5327e2981db00202e800a61ebc20085468debba0989da03166b0`  
		Last Modified: Tue, 24 Feb 2026 19:31:25 GMT  
		Size: 93.6 KB (93581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5150c7045bf1b315aa63ec5761f3ed6e74c3bc87a44a95f9c3cd27afbdc601ab`  
		Last Modified: Tue, 24 Feb 2026 19:31:26 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:647b074859ed9a43a4c318055fef73f0d964a094d238d403d5780d88bec95f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ae27a61f6170252119f48dcc0d18dcd47f07be5a66e40a041e650d2c209373`

```dockerfile
```

-	Layers:
	-	`sha256:14c11a2e503e22219769189f828eb275ea99b258385105689e1672b128fdc0f3`  
		Last Modified: Tue, 24 Feb 2026 19:31:25 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3cbb51a9c683a3e2e3a643bd8ddfc38a4459cab66b6383b95606445c119e2b`  
		Last Modified: Tue, 24 Feb 2026 19:31:25 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b18eee6fffcce65dc350cd312462711e19a5486817e474d2cd5f4c33d0e7541a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbf2213f97af3c182eb4956be399e5486fd503b35bd01b17c75417625c14760`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:26:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:26:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:26:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:06 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:443394a7d911f581670ce4df7959c82f7e8f0be02b5a7ba3c71bc5958012963d`  
		Last Modified: Tue, 24 Feb 2026 18:41:48 GMT  
		Size: 49.5 MB (49477853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fe7032d353de898b65d511f2a1b21d6d27d45325bdbafb18f4874bdaf053ef`  
		Last Modified: Tue, 24 Feb 2026 19:26:14 GMT  
		Size: 11.7 MB (11692913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d5aae81cdcbfc3d2a52b4b768d480e98f1b34954e2e3b5b0507d807246fce4`  
		Last Modified: Tue, 24 Feb 2026 19:26:14 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922a1a53af6c957e821fd2c3fdca3af49066e00cdb5a80d841c3312ee389754a`  
		Last Modified: Tue, 24 Feb 2026 19:26:14 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd18a77f85555a62b345dfd68f6ac1fe87fd16ef2172ca2ca9c5027b026be8e`  
		Last Modified: Tue, 24 Feb 2026 19:26:14 GMT  
		Size: 93.4 KB (93410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1063095c1338134d71616e6b49b809830055bcc0bd96554d88fe7bcf42f59466`  
		Last Modified: Tue, 24 Feb 2026 19:26:15 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d572c2fdd7cc3b21bf5083163463d81276104fa2710be4448a7a7211aac263b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531cb6e10afbc2367d0ae41a003edc7dfc35e1a97b4ae70336b5f8eafe138671`

```dockerfile
```

-	Layers:
	-	`sha256:56761bb86c285cf399b522b144db0892e5084c6d85d2b52268976d03e2158e47`  
		Last Modified: Tue, 24 Feb 2026 19:26:14 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c5ed3f1f6f567d80c86687e6d5b7b3364be199cb637f6003e0d8b3bc2c02679`  
		Last Modified: Tue, 24 Feb 2026 19:26:13 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json
