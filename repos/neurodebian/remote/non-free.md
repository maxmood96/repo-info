## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:345bc7238b549e242190d82618dfc9f8e3d9b5d4eeb48d1f8f4c183b5ca39eb4
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
$ docker pull neurodebian@sha256:8bd6a40105820974efe39bacbacdda2abf45d9a2239a1ed59ed5cc08c8ba5924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68920c76da27386dc105718634961f0d847b5b71341d43ffa344575c779a5760`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9f38856aca84fc144c0894b5583b4733c356542f9aabc617530a97da355e93`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 11.3 MB (11266599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bedb0642cb91b6008a3795412ad5527c9838485628cdb532f1abb601b3d56e`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0eec48808fb3af2793b868bdf881c68d54ffa9e36a78a84d6e0d6b296635ae1`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62c22daa22d6e4428a915ba7f39570fb94d04a461d6f66900ed31435bdc8520`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 93.1 KB (93113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b709e37690577434c0e98ed93efe2e947903baf6645ac5a17f97519f11a05c`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:18f6f19cb34871157480e0861fe447601f5dbf2c0b53bdef2fad3d7fbac6c7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92278b6032691d9a3cb503369fed1eeef86279c73860d6a32164e168f0591d0c`

```dockerfile
```

-	Layers:
	-	`sha256:da9593be6b0b5f94837cc43cb8a00a54beddedf81adcb710adf290ceca381181`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 3.9 MB (3924279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e17459c208fdfbf0ed14c8725db4eea4a2aedbed0bf0ec8dc704592a7e1ead4`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:761fa3220c10853beea131741907ee20e70ec4521ac8bb053ed3102cc2c2f107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c6a24608f1cf51881701b2548227ae1a0c126c6ad59c7c32ae3e326410aa0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6516de16487e13fd76db87360111809c44b836a1dd673fa8de93b983583728c`  
		Last Modified: Tue, 13 Aug 2024 07:40:33 GMT  
		Size: 11.2 MB (11232114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6108c7a663d245cb0932ddfae87f92ca3e1de7fecebcc1c63ff8508adf4e6db8`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08a498a3c3c4bf8a5ccf542b868e62921588d0f25c6cc09bac0d6a005711aa2`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e20e8cb909fb4d46a63b2053a3a0c458af529d893341a678b2c4b75796cb9b2`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 93.4 KB (93362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce457b9d5bc4664f2ee4fea10d635db111976ec6879c1d1b65c5f2583dbe5583`  
		Last Modified: Tue, 13 Aug 2024 07:40:53 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:faf07f81a060067adb199891ec5a55de7b6b552d9e1425f1af3d811264f4ad67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b630765608bbb9375212b2673d9d41627e2f3fdad5f8105e334bc40f372814b6`

```dockerfile
```

-	Layers:
	-	`sha256:b5b0a3582701ba2dfcab416b724d504cf731b6eba018c782d7f8f980f48d5880`  
		Last Modified: Tue, 13 Aug 2024 07:40:53 GMT  
		Size: 3.9 MB (3924532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2796e687428634d360ff415826bf00c056a4a1fd7916d81eca260088e413ab5a`  
		Last Modified: Tue, 13 Aug 2024 07:40:53 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6dda59b69a60752417dc53a7da8941269d242b1e51024eefe430dc3c8678535b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62364011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6544912638a3d685fb71af9ef012ae48702e550f4eacecadc34616be26b1ff`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96a775276b452d08188a5c8cefb2671c2351befe343f1b71ec2831ff494f794`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 11.7 MB (11688976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cba750c7d48374c4a665b3aa6dbc0d35907c8f5351297534109e7710fb5c1f`  
		Last Modified: Tue, 13 Aug 2024 01:12:04 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4f40691f5b23aab625dedc59cb84165c3346c956f411c37faab61829e98875`  
		Last Modified: Tue, 13 Aug 2024 01:12:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f559b7b520cf1d9f632d590f4a76abef8d20d19ee766429dd08dfd1c710e99d`  
		Last Modified: Tue, 13 Aug 2024 01:12:04 GMT  
		Size: 93.2 KB (93188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3984a8ad3a3a24cb4c87f0a2b5e7d680ee45cfce31b1e5cd4e4f20f1155943c`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ef44f9fdf0ade8b16b042df566cce5c0d994e196038e8dc7afac19802fe5532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132b918c3187bacdd483261bb47116c101b17645636f69910a6307417710fc41`

```dockerfile
```

-	Layers:
	-	`sha256:46ddedcbc2ee5bb19f1be63bafb03eb6792a0d36311f43bdc4abca7f7d714bba`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 3.9 MB (3922196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b55d3c3b9f45b61d2f39e46bd54d2650bf8f8a7462f64277466dd89f98889a4`  
		Last Modified: Tue, 13 Aug 2024 01:12:04 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
