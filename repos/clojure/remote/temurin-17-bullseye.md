## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:1569bd1f8964df95a84b80528266c7aee0deaf2062ae0d27fb3ebd53a70baccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:907fc8fb777de0b5bddd0150ee58c4f5a3a4dd9add4bd9808699f9e9ce98e04f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294480636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5a43cfc1580682a7c6adf73141cf3985005f68dbdcd7717acc09c7522cf0ee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:56:02 GMT
COPY dir:09afbf947759009c57336c17f70cd71239c5d8b0170793151aec66483cdd0976 in /opt/java/openjdk 
# Thu, 06 Oct 2022 03:56:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 03:59:18 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Thu, 06 Oct 2022 03:59:18 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 03:59:33 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 06 Oct 2022 03:59:34 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 06 Oct 2022 03:59:34 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 06 Oct 2022 03:59:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 06 Oct 2022 03:59:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acfce48843835d39fb569ba75ae523857fdae8d21d473e9152a27cb419979f2`  
		Last Modified: Thu, 06 Oct 2022 04:12:08 GMT  
		Size: 192.1 MB (192137601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e2e0462049ff0618cd2ccefa817ffd0004dbb80d10cd3790c7380dca9eef05`  
		Last Modified: Thu, 06 Oct 2022 04:14:36 GMT  
		Size: 47.3 MB (47295770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0daa4f9edffb846700224545be0fb24f7798f7c02ca38b5fd036b4e53d1c56b5`  
		Last Modified: Thu, 06 Oct 2022 04:14:30 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b6f49c050e266c71bb828f6bd427ef4f8f84c32939d00b39c9185a9f45a29`  
		Last Modified: Thu, 06 Oct 2022 04:14:30 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ef28dd9bbf0756b174127f81ab7273501cffae33ee7ab76b1dd6b08f6b0d3cdf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291692626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c326d8433f4b2fa1016adcbce350970986b8df9e6cb82648f5033e4ecf66f24d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:38:34 GMT
COPY dir:dc2bc1e50ab42c5231433386b6bc2a9cff04b310112464fb4909efc66be10627 in /opt/java/openjdk 
# Thu, 06 Oct 2022 02:38:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 02:43:38 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Thu, 06 Oct 2022 02:43:39 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 02:43:55 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 06 Oct 2022 02:43:56 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 06 Oct 2022 02:43:57 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 06 Oct 2022 02:43:57 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 06 Oct 2022 02:43:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b7798e9e43d2494af502b188de7bd161f67c7162a0b931a6e81e4e8d7c52d5`  
		Last Modified: Thu, 06 Oct 2022 03:01:09 GMT  
		Size: 190.9 MB (190904332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22833ec855521cca04fc86b93d3b68759a916cdea47a12d1131e427cab330626`  
		Last Modified: Thu, 06 Oct 2022 03:04:03 GMT  
		Size: 47.1 MB (47086653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d639632738be2ded19909321c2a99801970780f2dd0fa3b2d1fcbffd171f33`  
		Last Modified: Thu, 06 Oct 2022 03:03:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462b44ba7912dc4885b93bbef8b2541703e963682f556855769a9263398e30e2`  
		Last Modified: Thu, 06 Oct 2022 03:03:56 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
