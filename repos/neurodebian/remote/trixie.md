## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:5ad1a1221ab9678504a9a9beba18ebbb40a7364d1422eee4d3f72a7fffeba7b7
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
$ docker pull neurodebian@sha256:6d762d79558c201d14a01e74573becee71d96b043ec7fea796724b17a3400d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59174533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4eefa4d71d13b7db1bbdfeaa1758a185409923e4363e732bed24ecf61cdf648`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a2a54a01545a139e680d47b64716d1b9faa13cfedbe015124f93c561b7c8cf6e in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:805956af4eee3ab822c97611cafc9a57a586c1386772c91babe5075c77f79efe`  
		Last Modified: Tue, 13 Aug 2024 00:26:39 GMT  
		Size: 52.8 MB (52841189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f663abeab595413cca77c6f88a50322c4f80411702f17a711185b2c60333f2`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 6.2 MB (6240830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75ad9f7a649edb3af0b7b6cc8889cae322c6b55fa769f8f9b3d620286adeee7`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06429724a765681651790d014b72d30be34a6ffa16992333196ce8b6362a509`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7641817998246bf51a0c4699044a33146c720f1df0e311b5d1b69b46516619cc`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 90.5 KB (90530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:37505ae8aec723614f36f687b143b321cb7caa64244cf45e5965d1e762c5bfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268d333f155cec535e6ef7351dd94a389f6929eae109a64f9245b9a7c04f3763`

```dockerfile
```

-	Layers:
	-	`sha256:7867a6667f51720c1d78329fb4253fa850c05a4d44cbc8ed22fbcf1189cbc955`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 3.6 MB (3560325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cc61e695b0ad6b83c0b832255d79ef2b109598a3fa1c29b83829c2b835647de`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 13.4 KB (13445 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:45bc1b5e04ca256a3094c23858b20fdce1c507bd1b29b0b8e5824c98f79901cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59338780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a457663f11cf1f18f4dfb55e7e6d29e9a7b19cc52067423fca67f1e7b7eb19`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:36c12887052d1b06bbaec01740a2cd1b9dab4bc7827e406c3311158554478418 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:493524e4a43f41421b39cb784ceebfde54145b94187eac6910c35f8178b410da`  
		Last Modified: Tue, 23 Jul 2024 04:23:05 GMT  
		Size: 53.0 MB (53026321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ddcf50fbfd15049ddbcb10dc63259476763e98b097bffa8a32df909bad91f0`  
		Last Modified: Tue, 23 Jul 2024 18:36:45 GMT  
		Size: 6.2 MB (6219715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3483aa0e91299a8856a36b0b796da1e56032f6bf6264a46bc561cc2396e5bb6`  
		Last Modified: Tue, 23 Jul 2024 18:36:44 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a293bdf5fe3adfbdf9fc137d610631e39fb5217f0ae782744d49b0ecb810a71a`  
		Last Modified: Tue, 23 Jul 2024 18:36:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00033a80d29cf074dbb5224456ccd6939491504875f91ecc06de897b8c7e05c2`  
		Last Modified: Tue, 23 Jul 2024 18:36:45 GMT  
		Size: 90.8 KB (90756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:376e6b8ebc08c698f9070bccffa5dbaae910eb06f287c399f0a66a1e603bc2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b582f3f8a0b06db108a39a5b9dd097dbe5c2564d4a5be963ff8d41dc10e545`

```dockerfile
```

-	Layers:
	-	`sha256:e1342257e0b7816ef7e7148994cb9dfc3cea41fd489f7e6208d4cc70d1b49c20`  
		Last Modified: Tue, 23 Jul 2024 18:36:45 GMT  
		Size: 3.6 MB (3561584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63601a096d77be57ad1fa6b9007d197b4192f066d720aa3377deb800e33ce73a`  
		Last Modified: Tue, 23 Jul 2024 18:36:44 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:2917d3afeb3fb636e12940beb6791076a7cca7bcc9323f0d210d2eb049517a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60435962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162543759a640728d99080bc6821ca27f669e5e6d2f194830250fa18d7d5ab66`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07041f7523e0901d7c47895945c0bd1cacb4692d4614b1ffdbe05fa57e01e4df`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 6.6 MB (6565982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca643e5a596b37baa07257045ef13923dcb3596dba7f1d83275b23371f8122c8`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248be0caa7517a9fa8f3ceae041a4a546ee6ffcb5a8e17da61311b64cef0f39b`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465fec9852b0db92fca39606004e3da1bff74c315b4ba1a49ae6f98bd4ce588c`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 90.5 KB (90497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:194159e51e60e4cd446bc9871b2b9dcc9c1939ec0cb8ae4a5be2d10f5da5b5b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da11e8ea5815e2cc0c24e8b7a74d6610b60031b2503f72b6a45eaead60b0e0d`

```dockerfile
```

-	Layers:
	-	`sha256:214c5fbd9973ffc5415fc3aeb6b5c3f3dfccbd6b98cc07ce869780e51832b773`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 3.6 MB (3557418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b25cf0ea84c2e63b9d10044e8b28a910dd9082e4e5f6fa9c44c115d782f698f`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 13.4 KB (13420 bytes)  
		MIME: application/vnd.in-toto+json
