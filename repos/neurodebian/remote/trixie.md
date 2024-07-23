## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:111066afff1cf55b71fc11820e1bf70e832c06db19b663e65946879d1a20c4ae
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
$ docker pull neurodebian@sha256:c4b81779c10398e7fe06a035dca38cd224ac16e3645a01acd85db78649dbb786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59137257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3678be57aa9d30360d8695e003711a4c831053fc502f54e607ba8149a51abf11`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:aeee476035b2ce2f3c795377011e41eae116861792cc7c02090d8c6e0e5b40e9 in / 
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
	-	`sha256:2c622000fb34abccd4a19243f49979fc534d754c97f8e18457162c25dfabe489`  
		Last Modified: Tue, 23 Jul 2024 05:30:46 GMT  
		Size: 52.8 MB (52821206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca506ff4506aafde8da4f21eb9a2f615611948d193d55f477560e72e88a04a4`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 6.2 MB (6223958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a501c5b0743ce37ee8f6bd0c5a7f3bbd2851b958fbac6133c82cfa57902b10`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a00bf503c4fa80a04227f2ed1c6dffcb56daf70572e1e4743abf42476c4d44`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544162e28a198dad4dfc9abc136e6b1c32aa8b6c688bb942bbdce3c8e6359ed6`  
		Last Modified: Tue, 23 Jul 2024 07:14:56 GMT  
		Size: 90.1 KB (90104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c0974df9b32ace9cd20072bb6d5a8e1e3e761d9fec7e1630c5ffb71acfa8396b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381571328f9c493079d456cecadf9934520da72a9dc06b4e1711040b0447b482`

```dockerfile
```

-	Layers:
	-	`sha256:2dc16c93ac20b71df6dad38c59949baee0a48aa143ef11aa088ae6a7f852a0d5`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 3.6 MB (3560542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2276638b179367c1cd2cf60c2dfef8230023447c2b757f248985a62e839486`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
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
$ docker pull neurodebian@sha256:b8766a69e3f032dc2f6b2cbe4d089960517e300fa667303031b1ca347e0530cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60327871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dd7d012d4427fdc78cc3d99925a826d93f30b2af108e1ff2259cc078e4d7a3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:01a40f7b1e06135068b561ea73bceefb80384e78cf04f7afc30b29280b89be42 in / 
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
	-	`sha256:603ccf6e4399370cd3c9b421529967f58d124fe253b75b4d92b2e58cf112fdbb`  
		Last Modified: Tue, 23 Jul 2024 04:01:16 GMT  
		Size: 53.7 MB (53681250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe93559091ca5d3ea9a2404a6a0041392e2d6a77c8c2175fb2fcf6d43b1a5dc7`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 6.6 MB (6554634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620e5ddc09f8fa7a074698278a93f275d8f43471e76f728d5565fd5208e6bf60`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e6c08312333a956a5d07c8006e3363f7c3602a92e9e7ae72ef8021a657d03c`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb757c0ceb60c7b92a16ddc5e134af72f24cc17185d5faed73fda17ed6438733`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 90.0 KB (90003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2c1eeb9815e16c9aa307b7a53c9ac453f52d051282d5ef3d74cf0329510c75c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1e7c9987235a5add1af665720bd726dbdb11d83f43866c2688489e7809478a`

```dockerfile
```

-	Layers:
	-	`sha256:77423ed85dee033a7d2148fb492b023f86649bb56b475ff1fc1f5dec2126ae64`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 3.6 MB (3557635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:954999e20fe2243cce79ddf1335de6381ab8bd1e102c7b7e5974800aad37ad99`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 13.4 KB (13420 bytes)  
		MIME: application/vnd.in-toto+json
