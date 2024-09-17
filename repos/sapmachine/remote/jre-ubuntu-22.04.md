## `sapmachine:jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:670e4fdd589f753d0f86d40ffdf8a9e09a3a0858f3ec0c1b8fa3ef8d7c9c4094
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:0fcd8e5ebaab1f7e08fe9ec2aae7c8c9e7ae422aa289224f88b859c6cbfbdac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88668814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ac795ef1785433c559d78cfd1364de06300531ab5482b1052e9a5e15f2399c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5945165c7c33703b215bf0e07800cade3f7ed43cb4b69a8fcd9ad3c075f1c516`  
		Last Modified: Tue, 17 Sep 2024 01:00:37 GMT  
		Size: 59.1 MB (59133126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:93bcf7d9936dcf29b8be3d7245490de90a61317c50e2bb56e414bd871b350fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93d4441d84800efbf9346a8c22ff1efb923e3f0ce15959a92225cc96b6d5be0`

```dockerfile
```

-	Layers:
	-	`sha256:d21d01ccdfa245f10614252def56307c3015f6d486e55e71f455f23021acada2`  
		Last Modified: Tue, 17 Sep 2024 01:00:36 GMT  
		Size: 2.4 MB (2390040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c484b3b5ccdcffcf4e55587616dd65252b1c66610c9c7368b7b5b37dbe041112`  
		Last Modified: Tue, 17 Sep 2024 01:00:36 GMT  
		Size: 9.2 KB (9209 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9c3f0ff029c02082a037d430704694203e15c0b66d65cbc8ce9834bf4cc877b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85493922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea35bbbd10afb09439bb313b78312232ad6359423326abdd7f1c90422400dd6`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
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
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4560712663f0c5236a3a9963035a8d5fd5c5f89b104e4f44011cad54ab4112`  
		Last Modified: Sat, 17 Aug 2024 04:10:01 GMT  
		Size: 58.1 MB (58135239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:36a607f67bd027ab647e98a16a23904f69f8bd5615c9725e9e9e40cd11985e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381e42677701b2703ec1bba9d587d62afa66ed205977dff6b3a5d90064a504e0`

```dockerfile
```

-	Layers:
	-	`sha256:607552cd1efdb9b167cca51c9e40291b83b93bbee106d9dd8ef86e253d9444ca`  
		Last Modified: Sat, 17 Aug 2024 04:09:59 GMT  
		Size: 2.4 MB (2389113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:570a0bfbd47e607843c2c108a564125303cae6045eb5442f4da58b0b79c57948`  
		Last Modified: Sat, 17 Aug 2024 04:09:59 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f72cc9640f4fea88db184fb811c9533726fd84ab7147bbf6d9c54eb0e1828b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95022225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef7a8a92fc0f73e858a9a2d42461c1743d4c6584def047e4fd8c1b46510ac4e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
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
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4b1e56385b2443536f3b4d7f71682a7e03f03ef3338ed662776b9e8db13f41`  
		Last Modified: Tue, 17 Sep 2024 02:27:04 GMT  
		Size: 60.6 MB (60573983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bac4968a66e39750c38e22f27a3e4b9815cce588cca3244f32a1af29abfa233e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483c69a4c8b6d916eba7600275d39815b42f15e3809fdbbc301ca78108c5f114`

```dockerfile
```

-	Layers:
	-	`sha256:f8f4db4dc67c20cc0f70d38b73e8684bd33b1fca0025a72ea062cf2034c6401c`  
		Last Modified: Tue, 17 Sep 2024 02:27:02 GMT  
		Size: 2.4 MB (2393400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f1cc80ae86fc112e7cd96702cff1734a8ad340e64a1fa48f4cd08e27bd7bc09`  
		Last Modified: Tue, 17 Sep 2024 02:27:02 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.in-toto+json
