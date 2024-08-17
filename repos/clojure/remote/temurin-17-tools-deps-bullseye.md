## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:d60cc9602a33cc610717051c274740f46d2bc226e728130164f28111c30919bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:879f79f8bdabd4305ed6dff66b84612764bab857baabb1d7af15618d99bae0fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269213018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e8d05b7a96009a928efd26ee4321facc0996f56c9f2e7b58fbe18978ddaa27`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8e0be8bdb00d8b0150245e261c25e450a0c819984f0b22514584538a31715d`  
		Last Modified: Sat, 17 Aug 2024 01:59:47 GMT  
		Size: 145.2 MB (145164833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c18bbbb7d99220017424bcc5f826ce2ad235a881bda82a1744422f99a7a1594`  
		Last Modified: Sat, 17 Aug 2024 01:59:46 GMT  
		Size: 69.0 MB (68962470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ede52ea94edc77c319ad34132e4ccbb378feaf7b0d944b4b6d45d750ada97f0`  
		Last Modified: Sat, 17 Aug 2024 01:59:45 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb82b31f8a966738963f9aa6969c775c7c0f8d173787714c73512094ea564781`  
		Last Modified: Sat, 17 Aug 2024 01:59:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b8c83c6f0eb734fef83ab5c9a98b219b3db36f1a378d5b8b41983a801c0b6b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7055783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f2302a01fdfe82ccdd8ceff0690637271d336e37b62a44e487f6758b275856`

```dockerfile
```

-	Layers:
	-	`sha256:cfdfb1660c689c2afadd0337a20d3d18ac4d70bc807144b09840e4dbea48b352`  
		Last Modified: Sat, 17 Aug 2024 01:59:45 GMT  
		Size: 7.0 MB (7040344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37a0b5a2156f30adbf095b63164d7ec8ef5c3b242d59ca6b593d2d276495b213`  
		Last Modified: Sat, 17 Aug 2024 01:59:45 GMT  
		Size: 15.4 KB (15439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fb753b13268534c4a2512c28957a0de8c0ad94331f903e971d96be16e7c15af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266783376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11646d2c29466a227f5e30bf82fdd010cefe95c57333b0e70decd436bf4019c4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a210b758a485c1774755ac4bcc763d9e5c2e79f4f313464143649f79d22d9612`  
		Last Modified: Tue, 13 Aug 2024 06:32:55 GMT  
		Size: 144.0 MB (143959483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae00da131343f70d704db9b53fd555ef37bd3a8085cafbd4dae3b0909260da2`  
		Last Modified: Tue, 13 Aug 2024 06:36:15 GMT  
		Size: 69.1 MB (69092931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c40ccd05bd2e17be986fff6c84aa0bdeb22ca56d65f2f2ecf9a18a0b3549b`  
		Last Modified: Tue, 13 Aug 2024 06:36:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ef84ee87f8794c5445c096c648074b3f980fbfab499c22f2dbd8b6a2ad309b`  
		Last Modified: Tue, 13 Aug 2024 06:36:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:379f081689ee15143ff2421ca92281666b77a3a973d78aad7c45884471563b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abde6d1a57c3bcd4e6712d89ebd7e34f15181ce249c79833af09afe901737e95`

```dockerfile
```

-	Layers:
	-	`sha256:7381be6e5e3aa4771d9542d112818a097094d8b965133f5361cc0b47a35d1f8f`  
		Last Modified: Tue, 13 Aug 2024 06:36:13 GMT  
		Size: 7.0 MB (7046066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27bf6fcc8063c2cada646c64102faaecde408c0f1dff54ff904896f4146dd95a`  
		Last Modified: Tue, 13 Aug 2024 06:36:12 GMT  
		Size: 16.0 KB (15976 bytes)  
		MIME: application/vnd.in-toto+json
