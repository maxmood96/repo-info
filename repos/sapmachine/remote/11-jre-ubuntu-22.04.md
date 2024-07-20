## `sapmachine:11-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:ccd92779e9ca78c1aec4e76ccbfd1bd32ab4e4475b284a65b3c9c4cdc56e259c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:7db417494bba678692d7a869ef7d73f06c19aaafd982a9deab45da34eb98d254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79490972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938af1bcd560af10c7ce39453a2eedd266ab60234b2eec6ee8413d4d7247d1b0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862f89c42d81f3e94179c7f89fd58d6f726fefdd953a4eeca1063f434ef3e12b`  
		Last Modified: Fri, 19 Jul 2024 18:00:33 GMT  
		Size: 50.0 MB (49956917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1561afcff2227771786435d3e969ddc31fbaae7fcc92e4f2e0f1e7737b178536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2407494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3f9db95fc2b92317cc7aef4beb1db6823c46e0bd82b3925c93008c9fde6b00`

```dockerfile
```

-	Layers:
	-	`sha256:22cb1b414f0ab5f4bf256184a189eea569db18d8137b4117c48ee4e271daac27`  
		Last Modified: Fri, 19 Jul 2024 18:00:31 GMT  
		Size: 2.4 MB (2398928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48881a4d30429497c8428a6373f777ebaa0eb903d2589f6d52cfd91bf8012002`  
		Last Modified: Fri, 19 Jul 2024 18:00:31 GMT  
		Size: 8.6 KB (8566 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:57646a99f4303af9636072b26fd11508945e4d9b0f452c72962b36fd6ba1329d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76599582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17cc4a116fecb24684f17b3ea1b319b5e327e17f09b2db8568ba58af7389d52`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4484468fc0c06949f4d7187ef7572f5df7ff37524c360fa6e17bcc3f51cec0`  
		Last Modified: Sat, 20 Jul 2024 00:39:59 GMT  
		Size: 49.2 MB (49239557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f2e2d07832c6225bedb131101fd5c35a0d7652fad3444caffe95d7c2fa7e4580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2408104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c34016b397185e755c8ea7d06ab7b07e577ef0866bf3bc0a7f0aab9bbf75dd`

```dockerfile
```

-	Layers:
	-	`sha256:1ba2a4fe41f504225215f80d0af39bd756f2ad3004c26f063a5fc5796f39023f`  
		Last Modified: Sat, 20 Jul 2024 00:39:58 GMT  
		Size: 2.4 MB (2399236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cef28ad84b4c703b87bd7f0590fc293ec61998908da4593ffadcbd83302e7dd3`  
		Last Modified: Sat, 20 Jul 2024 00:39:58 GMT  
		Size: 8.9 KB (8868 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1b3c455292af14609b993d1997fa84d70d12ac3760c801cc0b32e208b9119471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83046198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98dbe7112529c5640fcab1250ec0dc764edccb3038ab87a3259c5f654c004fb`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5820fb456097af9567cb7a2fee064ba4f5abccb3cd3ff93b77e6fe3b59812738`  
		Last Modified: Sat, 20 Jul 2024 00:00:07 GMT  
		Size: 48.6 MB (48585117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ab761ba0b4ae1fb1b04f468d3dd49210d8434cb515e0b117046d54955112588c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2411518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d140be5d253b06ca7cbaf85918071533e2ac1f7642d16ef4c5aeaada996383`

```dockerfile
```

-	Layers:
	-	`sha256:5dcdfec9af6b070417c5cc3a0af163f777235ddd299471500b98614a336c4e94`  
		Last Modified: Sat, 20 Jul 2024 00:00:06 GMT  
		Size: 2.4 MB (2402913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79387db1ec97f29efd833eb61878c5327d9b64432e8071e50ce833d022b9e287`  
		Last Modified: Sat, 20 Jul 2024 00:00:05 GMT  
		Size: 8.6 KB (8605 bytes)  
		MIME: application/vnd.in-toto+json
