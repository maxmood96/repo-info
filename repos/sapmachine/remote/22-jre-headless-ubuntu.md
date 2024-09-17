## `sapmachine:22-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:8c69075a13b2ee6751199c2d78265b7b6e01b6d7a36a441c5ef9a327b8803524
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:46716eddad12eb8bbcc3c7fa36ef12e74f7b25629f72ad3e217cb389d289b369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90478590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94149e635910e820eddc635a2f13877fbcb932c535071f1f053fc682c0dbc12`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:d743a32465d8eefee7d0eef080018e2a0ca198147a6389219a4d6fc4eb4d7807`  
		Last Modified: Tue, 17 Sep 2024 01:00:48 GMT  
		Size: 60.7 MB (60728762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:860cbdaf7219fe764654e26870cf8070597ff565feeb7887617a4a83723e47c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690581e6cac4bcd056fd7c78232c47d5e3486cbcae0448829aeed296ac6d0d88`

```dockerfile
```

-	Layers:
	-	`sha256:d2295efa9adcd69cfef6559c7967855289ffd031d3cf60d6745a04537c6af919`  
		Last Modified: Tue, 17 Sep 2024 01:00:46 GMT  
		Size: 2.1 MB (2130208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9aae2f84d9c9c0e9fd773b82573be73b89bc08519f1ef32da2ae7ee447f159d`  
		Last Modified: Tue, 17 Sep 2024 01:00:46 GMT  
		Size: 10.4 KB (10372 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:48108ad8ae386bc22924c6363ceb75dfbfe3185129d7ef8e873ed9ca4e20ff24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88475446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b40a309a08fc549477a41d5c98fa5fce4b22e671bf878eea3296d1b3a0e702`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:69e8c9105fb2f09cde268c1df60a6cdbd4d77d965450bbe5158ed74c24b4197d`  
		Last Modified: Tue, 17 Sep 2024 03:11:53 GMT  
		Size: 59.6 MB (59589847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8e75321cdd7dbca11f8183bff75d7998ca1fe61991671092e2568a9f77ca15ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c211b0e4b70051f396a79bf81178d5dc1624e38b70a089afba1f9b4f97982ae8`

```dockerfile
```

-	Layers:
	-	`sha256:4dc057dd37120db2d6e25119edb7cd70773a21752df8c11411a4947390825f9d`  
		Last Modified: Tue, 17 Sep 2024 03:11:51 GMT  
		Size: 2.1 MB (2130095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:938e5b60846527fa025e21f829a6abb5929c331d5da68c15f24670bcdeb2eccf`  
		Last Modified: Tue, 17 Sep 2024 03:11:51 GMT  
		Size: 10.7 KB (10734 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:500928f5f04d96297043ca6fb5ac5951ebd606e848786d7e95c43fab0ccd5ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96722356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6a08157804ca84658ae15d694260fe2d7ed0820fefe24ede1f9b3ba04ff61e`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:92fff0ce6b23f0d52c03241dc18205a19015d2ab1fb22114a228b3f8db8648dd`  
		Last Modified: Tue, 17 Sep 2024 02:21:35 GMT  
		Size: 62.3 MB (62330011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:231d0fdb8ea6c3978eabc76fdfeb13fd0b4149becb150763cb0e62e5175bb5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c52c962b035664352be24ffedad495d06f4ae1ee01c123d769ad51fb87afef`

```dockerfile
```

-	Layers:
	-	`sha256:7ed7e31da31784d685af95d272882e464441be552621110514f1e12ebe78fb85`  
		Last Modified: Tue, 17 Sep 2024 02:21:33 GMT  
		Size: 2.1 MB (2133481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f6a55154675f521803deaaff72b3f50072f53612474519448c97f0c4155d8e`  
		Last Modified: Tue, 17 Sep 2024 02:21:32 GMT  
		Size: 10.4 KB (10441 bytes)  
		MIME: application/vnd.in-toto+json
