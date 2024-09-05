## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:90cf4dc7088dffb32b85b68fe7363c1965245e41ea69dba372b40c540f24859b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:375551e0ee464227926c04aded547c9ed079c415c889c721accc40be4e7812fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227790825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04de7fc6eea8b5b1471d32298cfc3985fbd354c57c42c67858e7a0e069a91977`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
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
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee80b11682ec0aac86c8b4814e12b5bc519207f79c40360f234ede7732ce3b6d`  
		Last Modified: Wed, 04 Sep 2024 23:07:41 GMT  
		Size: 103.6 MB (103611881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d5a6b7a85b2e7c5f776b74df78f788b8a278762c53e7e21e91796d941ad49`  
		Last Modified: Wed, 04 Sep 2024 23:07:40 GMT  
		Size: 69.1 MB (69096969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f239025a9efd973e977ca4bdcdc9084886c1dac740213b179f37ba3cfdef5370`  
		Last Modified: Wed, 04 Sep 2024 23:07:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5ed63e60e1cd84f915dff1cc0b4112f83beb38f3e775f3e0b4234c4a741aa0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7079687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c365a1ed4009a756dd6547ccb4029f713cba19cf1e55600732ab4e1061784253`

```dockerfile
```

-	Layers:
	-	`sha256:b45e729bf8ae2caa493b3c775f5b056bde46e624a41ed2714104ea194ad38e00`  
		Last Modified: Wed, 04 Sep 2024 23:07:39 GMT  
		Size: 7.1 MB (7065835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e0f9f4db80343b192e145b05e986bcdad178c1276e2ccf15ccbfa964f77fc0`  
		Last Modified: Wed, 04 Sep 2024 23:07:39 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

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

### `clojure:temurin-8-bullseye` - unknown; unknown

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
