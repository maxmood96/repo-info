## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:af7cc6a188004a5fe3e37ac3e24d3daf4efbde5e28a11783e98ae7649dcaaaf9
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
$ docker pull neurodebian@sha256:8ad50c552d2d9ba9971607e3e25fcff5e656fe578bc84e4ebd7fb18738512adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b4c5c48066c6bab18c83db1004c63f2276ce263810a3b47cd0e67ca0e5d0be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0c4964b2c74b33113f4f9253f8fdbd6f9effb7070fabfe7998ec7f9f71a68c`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 11.2 MB (11231990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a84d3037e0ebe02d7b2e60abbfa3c50ab185daf05e3e55e3f8ff6cf96a45b2`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784313ea4757f773fd668b9d92e36d3061207f4d5f2fc7c75d857979e14d6f21`  
		Last Modified: Tue, 23 Jul 2024 18:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f51ef3b42547d51fc5c3da2f3e174e60effa7629f2f7e46098c454225497cd1`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 93.1 KB (93109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a89e8d1db6d68a3f2363d7ce074b5496e4fa63f099ca409686e3f84f30ebda5`  
		Last Modified: Tue, 23 Jul 2024 18:36:05 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2d20471e880f9bbd6c72aae7179ae7d0d26c0ea16bbfc67999f481fe78ad46d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08416b7a7fa5ef781f905251ee5d1a660baae6bfaf1e10c86a265115cf1660ef`

```dockerfile
```

-	Layers:
	-	`sha256:01968acc1d8a7282a89c4b803ed512cd39f8497d1768e0cf330e008a56dfdad1`  
		Last Modified: Tue, 23 Jul 2024 18:36:06 GMT  
		Size: 3.9 MB (3924532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c13697cc7290159bcf6b045e62a67f922b62336ce65509f7615633065b67364b`  
		Last Modified: Tue, 23 Jul 2024 18:36:05 GMT  
		Size: 16.1 KB (16113 bytes)  
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
