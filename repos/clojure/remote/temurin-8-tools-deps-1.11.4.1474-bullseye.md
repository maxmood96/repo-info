## `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye`

```console
$ docker pull clojure@sha256:6b92bdd3ebfc58a495ec880e40625083d9f69d79cd2f63ae8668323dd1a6d096
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7363412dc15758670bd12028061370516fa713c36eb1cbbe1f9d2d6d85c70cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227659950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea97f5d66a966bebe8820da853ff26d3ca3a5efd828ead5ab0c23470011837e`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d99cb668ab7f02cf1b20c35f38a8e0884baef13a7f168968ff4893090a5a014`  
		Last Modified: Fri, 23 Aug 2024 20:02:04 GMT  
		Size: 103.6 MB (103611892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72eff39293ce0495fd699214b38c5e1437cbb6a7c598fd0893e4434ebe97ec25`  
		Last Modified: Fri, 23 Aug 2024 20:02:03 GMT  
		Size: 69.0 MB (68962736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b684199b65797111f4e7cb962e5f3d29c206b4c2d8ca43fb93356d8554c3e0bf`  
		Last Modified: Fri, 23 Aug 2024 20:02:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:55c422bc1850b1a0dedd50f639cf01e8577c6983d5836c83443f0786f63725ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7079687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26834ebb07b2797951b07c00ab57fa3333fe9af50b4d1953d7db8cb446e49356`

```dockerfile
```

-	Layers:
	-	`sha256:f238a3307ea8843f51c281ef6ab5e03a83b2ba4780cf958706b1688a479b912a`  
		Last Modified: Fri, 23 Aug 2024 20:02:03 GMT  
		Size: 7.1 MB (7065835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12ba7a5e1ce6c41a5500f381546e7042ff2980d151a21169ffbab72c67241385`  
		Last Modified: Fri, 23 Aug 2024 20:02:02 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:894a63e8ac059d300dfccba079110f03d813bf6bbdb84f67b808e83a0f7afe02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225553342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae5ba51ac14ea514af4a3b73a4be1caf177d0a2262a09cd2f1c406b595f6d06`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5737429281d133cda0b984ae6835507307684f383e03361e715daae49e451af9`  
		Last Modified: Sat, 17 Aug 2024 05:52:41 GMT  
		Size: 102.7 MB (102729249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0708b09d0b57624ac4c82245d971bd9a080248473e7c8fc17ea34b7b2518de3`  
		Last Modified: Sat, 17 Aug 2024 05:57:58 GMT  
		Size: 69.1 MB (69093527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919dcd43e7c7d71214ff87bce87ac8cd3b4b62456491473e8c0b1c743f6d6106`  
		Last Modified: Sat, 17 Aug 2024 05:57:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3593d70c0358ea801c0155d608f56c05b2131306e9ebed01bf35cf651bda42b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7085944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdecd1ec461e94c98753c05d911c078434929f6693703986b14ffefb9c58fcc4`

```dockerfile
```

-	Layers:
	-	`sha256:2e51472807ec0684116f2c8833329a287b597d2196e30c0b749d8cc2cc5a3025`  
		Last Modified: Fri, 23 Aug 2024 20:47:58 GMT  
		Size: 7.1 MB (7071557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c43270f43c02497824379d1f499435cc9453a3f71177134c3fca43dbefd9c5d`  
		Last Modified: Fri, 23 Aug 2024 20:47:57 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json
