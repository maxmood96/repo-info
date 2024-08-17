## `sapmachine:22-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:1c18a4ff496732bf9e1de376cd3c1e57fdeb6d0f5c0f71d5487e904ff22f62b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:91e0f39e905c9a2b673ac3fd2405fde693ea9973f55a5c1016c2e91e34634d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89215111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8902f6d367d17e01b10aca6d1ab31813e328e03c0f411175134a03618ba1faf4`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2283ad9c8833701e7a83547a4e809f1223c30a58026c81f08a82ce6238b2a5`  
		Last Modified: Fri, 19 Jul 2024 17:59:01 GMT  
		Size: 59.5 MB (59509958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:71b1d3f59dfd373446c0dd37d801283f38a78ed04e40a58f707b8f1d14b772d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76579578ae83bbcdbb16b38aab0bd0b74588b340a1fbe5676c45c65a6cdf166b`

```dockerfile
```

-	Layers:
	-	`sha256:6bc6f6261b9c7eb63c7a8f7ce88288e341a25b6876e01b73bcea481f9bb876dd`  
		Last Modified: Fri, 19 Jul 2024 17:59:00 GMT  
		Size: 2.4 MB (2363691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02a502c015bdf4aeabbae7481aab10f782c9cd8abf0f6467839895b0ccc5740c`  
		Last Modified: Fri, 19 Jul 2024 17:59:00 GMT  
		Size: 10.2 KB (10171 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:313f1746a8933bda9ad04c1c445a440f92de6f7d509342ae7f95d6fa725d8b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87416304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164b9aa35648a1bbf6ee0af838397e5dcedfa56fcec074702e32e8c6465c4868`
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
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcc95145b833b329443fec77eb9d12bdfd4ed858a5fb37e285e239f774bbfc1`  
		Last Modified: Sat, 17 Aug 2024 04:05:59 GMT  
		Size: 58.6 MB (58572618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:95d2f661aab60980a205bcffe7149b3acb7d3aeb02ead3f6214c3b5464068765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425c8c9eb89348bd3a614704ada7747b0e150f3925bb3ac41385e2d262805df4`

```dockerfile
```

-	Layers:
	-	`sha256:031be36323483b57a28c5ad493508453a6be76c915a47aad331e84e4c7677a65`  
		Last Modified: Sat, 17 Aug 2024 04:05:57 GMT  
		Size: 2.4 MB (2363587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74c72099aa625eb60e402e3723645122cbecbfeff56391e273c1e271e051bf8b`  
		Last Modified: Sat, 17 Aug 2024 04:05:57 GMT  
		Size: 10.5 KB (10533 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:15d69e18bb4cdcff177da299da6f8fc13892a28cab727c1025802694cd35d099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95600111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce1f8e456f692a67e533d1ee5b3994e26574935ec0737ab1894346245eaeb2f`
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
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59572b7d997deaf079b8387114a2b16f126407c4e48581581e20d3875a1e573a`  
		Last Modified: Sat, 17 Aug 2024 02:28:59 GMT  
		Size: 61.1 MB (61092539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ec9ed9893c5dd4778735d22439ba5c3f4216e75d3f0f607bbe16a8c2e160534b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5bac48eb47f7472758492245e89965e41d49b39fd25d7abf44f86b63f10884`

```dockerfile
```

-	Layers:
	-	`sha256:d4fdd87651acd4635c72eeb73a8a6a7e8904ad1d5bae76dc811262214ddd1923`  
		Last Modified: Sat, 17 Aug 2024 02:28:58 GMT  
		Size: 2.4 MB (2367027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0fc3110d0ba8f19f6cbee6c7f107ec0de7d998dc5818fd8c411784905759698`  
		Last Modified: Sat, 17 Aug 2024 02:28:57 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.in-toto+json
