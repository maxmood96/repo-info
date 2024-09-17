## `sapmachine:jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:adb5d6bf84356f6c404e52dfccbef862b470bf384c74d1847024d1a05241a5ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:65f762944bfeab24666fb06f56a30b16538da9a828d60f92f74adbc7c1a0ecfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244572206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1213ffecb0dcf5fd98cff886513aed168bfeb438f31da82c09fdee8484acea1`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c50c42711bc6c6751e9a81c728af05aa2becf8d0942c062be1f0f4caedc13bd`  
		Last Modified: Tue, 17 Sep 2024 01:00:51 GMT  
		Size: 214.8 MB (214822378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:66afcf0134d7ad70e9c13b9794cffb4ae1a4ca69fb98f089ed45d34a90b52d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2224223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb124f33d0f41bf42cd700a63c1d7e45f01002616c1057a4472b855180dca7d3`

```dockerfile
```

-	Layers:
	-	`sha256:142e73870863aa4846e7ef78fbb9901d7ef9a63cdec3be5aefee1ccafa7dbec4`  
		Last Modified: Tue, 17 Sep 2024 01:00:47 GMT  
		Size: 2.2 MB (2213849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88b039ed98035ff5213056dfcf9197e3b4033245e3e619865a95eb095fac31a7`  
		Last Modified: Tue, 17 Sep 2024 01:00:47 GMT  
		Size: 10.4 KB (10374 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ebcda09fc84a21bc4c56f3eadaacd83b65c2b5d5c120de3e4e9f6afe1c5a00d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241516572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1685b2f21d7e595a53ac3971d8a6f039551bcc1040a9f90307e693381dd7c63`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4800f9ecb1e7a7ba74b0b2b315f6338f252572ffcaf9c050df5bebca675e6ea5`  
		Last Modified: Tue, 17 Sep 2024 03:10:04 GMT  
		Size: 212.6 MB (212630973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a4b324778bfc1632b7db45467ab610965b519fffeebbe98e68fd333e3ea63464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2224471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68beb5bb1e99331fb6d3550623a6774ca00cdd55929d39790757075790cfc580`

```dockerfile
```

-	Layers:
	-	`sha256:b850ead18760f823601d291f946d6bdb6b328c88be6e61ba97bcacd1ec363674`  
		Last Modified: Tue, 17 Sep 2024 03:09:59 GMT  
		Size: 2.2 MB (2213736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c08f67adee2a01f9fefadb398e51f36bed42ab395676f36cab9e7f7a07905db`  
		Last Modified: Tue, 17 Sep 2024 03:09:59 GMT  
		Size: 10.7 KB (10735 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1df7c59141e68829b74c9bdd60d0166e07b2a550483fb4a6ea83223c1a86a69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250456877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad491a5c3ab8c051ed4ca261ec6ecc6498c5413178f0403295aab2d98c743c4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c526398e5e771684dae49961d5a74cd9606dcbcf7ddafb1fcc1433293927dca4`  
		Last Modified: Tue, 27 Aug 2024 17:08:24 GMT  
		Size: 34.4 MB (34392345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b17e0e9fd2fa123f28fefc5202d6b0c674cfdde53d4019a450a8edddf82cf1`  
		Last Modified: Tue, 17 Sep 2024 02:18:41 GMT  
		Size: 216.1 MB (216064532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:17d7be50d01b12d53639ea748f610ed0b1db6b76a2cdc7df45858dcf31542b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2225627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd72029070a9e47b82432af42938ecdc71893c774b91dd6a3eb9854f963ecc76`

```dockerfile
```

-	Layers:
	-	`sha256:a5d1958f52c3aa580740419a20cae9980cf2ac238dbbe1d49be69fdfa9ca4302`  
		Last Modified: Tue, 17 Sep 2024 02:18:36 GMT  
		Size: 2.2 MB (2215185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a52c0d8993de1c79165e67b3cd34f0e87af563447c71af7c5dbd5aeb30d795a`  
		Last Modified: Tue, 17 Sep 2024 02:18:35 GMT  
		Size: 10.4 KB (10442 bytes)  
		MIME: application/vnd.in-toto+json
