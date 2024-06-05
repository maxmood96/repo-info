## `clojure:tools-deps-1.11.3.1456`

```console
$ docker pull clojure@sha256:2f7fc0e438e574e2e648bd0a92254cf3089630aef97b1097e1f3ed09ab5da193
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.11.3.1456` - linux; amd64

```console
$ docker pull clojure@sha256:24d567f0588063dc7bf8ff1472936a40803b71ffdd1a714797579a6781d01cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288374120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef637ec94e2a5dc060d8dfdf66daa85872429c8a36f9b2c4faab3c532f4e02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad246211a32d46848be9601189d9208d315885aedbe572a849a9c4f66e28a555`  
		Last Modified: Wed, 05 Jun 2024 06:10:32 GMT  
		Size: 158.5 MB (158497970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d1f2a4fe702ec4da105ca3d2ecc8506cbe8d17e232f407c66b58deb693bc7`  
		Last Modified: Wed, 05 Jun 2024 06:10:31 GMT  
		Size: 80.3 MB (80298717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc8f69844e4d9c9006da1bc4faa60b9ced5b5fbcd4ed048deb78e956816c2a4`  
		Last Modified: Wed, 05 Jun 2024 06:10:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb947bda822c6494016a0bbc48473c4010154cdc047178df10a8660b512ba31a`  
		Last Modified: Wed, 05 Jun 2024 06:10:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:7fb8fbd04339319c463192332d497d344c62ef038172b6745c0a2cecaf8ae60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817a75155f6adbf140844a16cd345edd6f389fb91890e28f5eb4ffb1dc097e55`

```dockerfile
```

-	Layers:
	-	`sha256:2633d806ea5df3fa497eab6d4fd99bbda5f3c509a766364b1b225034f21ba5ff`  
		Last Modified: Wed, 05 Jun 2024 06:10:29 GMT  
		Size: 7.0 MB (6962676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f84ac94ccd3f8aff6c572d02fdaf305b90ba7b2b9d11716bc32e950cb40d3b8`  
		Last Modified: Wed, 05 Jun 2024 06:10:29 GMT  
		Size: 17.4 KB (17390 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.11.3.1456` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:277a53195214d4da7b7ea8359d9d7db223ff716e2985e0416242ae0cd8232756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286324475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d710789046d40916be8e6c0d3a2c47403815374e6a582c7b057d55d5d4a79f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182da03c0c64362525dc464baa408c8c81311176d1e88d579392ec6c765d9518`  
		Last Modified: Wed, 05 Jun 2024 13:30:16 GMT  
		Size: 156.7 MB (156665634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cd0b29de152e63b4e2dabddfb51cfc7084a35c2fae264629d03660f714f52d`  
		Last Modified: Wed, 05 Jun 2024 14:15:44 GMT  
		Size: 80.0 MB (80044403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd33477a08822723b7865c333e119f0dd23a7c9c3b67847b920483845fc3126`  
		Last Modified: Wed, 05 Jun 2024 14:15:42 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c451cf7009414678948b67111ace1419ffae1a6a85355e6713ae1667eee7c6c3`  
		Last Modified: Wed, 05 Jun 2024 14:15:42 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:a0a763b1cbfdbb2654455b90ecf59d3d123695360ac1a3742c4b65aabc5ca39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6987133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3235bcfb7e0be010fad6ed2bdd92b875f5c5819e60ceee20d406188df5387be`

```dockerfile
```

-	Layers:
	-	`sha256:ce27a2120be3d64f10bda1501ca0bde21d2e7903c6964f7a877d354dd66614aa`  
		Last Modified: Wed, 05 Jun 2024 14:15:43 GMT  
		Size: 7.0 MB (6969135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d5da1207d127672c6962bef1c8becd4e0cc4724c0677b19c5a448ada47dade`  
		Last Modified: Wed, 05 Jun 2024 14:15:42 GMT  
		Size: 18.0 KB (17998 bytes)  
		MIME: application/vnd.in-toto+json
