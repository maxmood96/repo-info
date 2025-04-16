## `sapmachine:jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:2f15d48f772a3c4d5ec19566b40dcce59751eb2e391b650cf0038e1c6c081c3f
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
$ docker pull sapmachine@sha256:f3fad65c06b41735268f4541338b5ade74c8fe5f090d07668f5c6b8605a44f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (260975800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c7e3f932499de62e6aa53db805eee3dc16aab12341b04d957f27e581538c15`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2010935ccaff4854b3e56928995fc516dcc9296dc420ffcd80049840335450`  
		Last Modified: Wed, 16 Apr 2025 16:13:50 GMT  
		Size: 231.3 MB (231258148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d2f1abd2b920ef0069881469d0a995cba32cf12bf428ca6013d5ce9283802cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2235835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766d619a495757b805929b6e0d85358b60af4f4e704f1e9faf2440f288737ef8`

```dockerfile
```

-	Layers:
	-	`sha256:1625e5bcb1ee6948e9883eb63c5cdebb91ca01ab3b24c824cc1a5fba2117864c`  
		Last Modified: Wed, 16 Apr 2025 16:13:46 GMT  
		Size: 2.2 MB (2225207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9198598f7266a81eb8d95ddfc2b15234841394f36dd772ce12066ee3d8637b5`  
		Last Modified: Wed, 16 Apr 2025 16:13:46 GMT  
		Size: 10.6 KB (10628 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:97c0b4e2d83fae7c6789400fc80bd84920b5cb885ce072f4ecb72d4433acf3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258012553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2d0637d1b87f57c232260702dd88ba98d763f7d37d8d594c23543ea6aa112c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1d5cb829c802ac31c11a630ffa933cc83bef494bd5f642f10345be5205fbdd`  
		Last Modified: Wed, 16 Apr 2025 16:14:53 GMT  
		Size: 229.2 MB (229165595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:790cd46cbeccd86033b7b0dedd8b7e6dc1f2dba08d6fb23fb0586fab732331c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2236515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082981f7accd7599075dfe3a788a3c192a209d3b3551b62a580468b7b5397af9`

```dockerfile
```

-	Layers:
	-	`sha256:41a10ca6585077cbba7402193c04c18c8f5ce7e52281004669729ca2679bf8df`  
		Last Modified: Wed, 16 Apr 2025 16:14:48 GMT  
		Size: 2.2 MB (2225723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf302dfb222e1b789da70d4622dc125dedc295160e62ff6e8b232ccf88dffe29`  
		Last Modified: Wed, 16 Apr 2025 16:14:48 GMT  
		Size: 10.8 KB (10792 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4574efb27bb3edaee6519cb8483754a3a5e3e89882b7e1d155bcbb72743c2065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266717865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e2d40b20fd410e378c2320b8528f5096616cf0722c355e3d9aa7d58e014145`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e58b251e8c2c5b287448b91f444dd3eafa22e2fbedad65b408f4393b06f9f16`  
		Last Modified: Wed, 16 Apr 2025 16:17:11 GMT  
		Size: 232.4 MB (232376998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ea2acb23167c1ced4cd7a211731e7a485a6a630d295db4d9b230264973196846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2237251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0b6fd5ae17d180700a32e329f82f68067d204f1f19cb4cd1a4312a465abf45`

```dockerfile
```

-	Layers:
	-	`sha256:0eab5b6d2b428ce24ff12fcb276bca6e9359a6663ccac5ab47b81562798c6ed3`  
		Last Modified: Wed, 16 Apr 2025 16:17:05 GMT  
		Size: 2.2 MB (2226549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9768dff0bc700b0ab74a83d3db94258a3f5e03635f20fb497c1bc0859788e1e6`  
		Last Modified: Wed, 16 Apr 2025 16:17:04 GMT  
		Size: 10.7 KB (10702 bytes)  
		MIME: application/vnd.in-toto+json
