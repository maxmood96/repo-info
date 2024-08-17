## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:516c26407d5567d3d68713cd0dbdaa8fc3f17895496ea7f9774704e2301a56ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:833c4459161205ba7d5aafdcb940decd43f296856d526fa1092542b8dfcd9a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227659662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a774a854c2a6593d03bd51da09678284221932a13ac452d35fca290e5069f985`
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
	-	`sha256:80a82418ff8b429bc00eda0b99d45e66e216c0be4e195966887eec2fc05d6aa3`  
		Last Modified: Sat, 17 Aug 2024 01:59:26 GMT  
		Size: 103.6 MB (103611892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d705833bab27abd59f1c778c24121e8b5a028cf38f0e489f00ebafa2bb738d`  
		Last Modified: Sat, 17 Aug 2024 01:59:26 GMT  
		Size: 69.0 MB (68962451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d47ecf9cc4bbbaf3f4bd62f6b39ea160d118499fd9f04c4b7f91f1027078b0`  
		Last Modified: Sat, 17 Aug 2024 01:59:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:19412e7b9654e50928d6826f6a5583a0f4978b41d4b43b10210ffa870a1ab6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7079687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d01bf6360be2a1823e0ca7c6351fbcf8630d6cdeb1766a1aaf269caa3fe074c`

```dockerfile
```

-	Layers:
	-	`sha256:a47bffa4873b69c91766a654366939852307f5482b10d402789dbc130130fbb6`  
		Last Modified: Sat, 17 Aug 2024 01:59:25 GMT  
		Size: 7.1 MB (7065835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0159cb79f0b3c420230e8188b8fc6acd4e919f0b9baed6068be433ccd6e36d82`  
		Last Modified: Sat, 17 Aug 2024 01:59:25 GMT  
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
$ docker pull clojure@sha256:2ebd70a35c87ac761757a296c8d5ea89540d6c3907e39b1304fd42a1437dbfc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7085943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d186bcfb0baa9ee07f172cf886e0dda83935925a7a01e98b6c2797f5436d83`

```dockerfile
```

-	Layers:
	-	`sha256:80a926d058cff30d2a2208b3b6db9873b1d9245556bab723fb74d1362938ee53`  
		Last Modified: Sat, 17 Aug 2024 05:57:56 GMT  
		Size: 7.1 MB (7071557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdeb4c81ed7d65feff28caebe49da81adb8a794b6c1c0b987a6092017d9318ef`  
		Last Modified: Sat, 17 Aug 2024 05:57:55 GMT  
		Size: 14.4 KB (14386 bytes)  
		MIME: application/vnd.in-toto+json
