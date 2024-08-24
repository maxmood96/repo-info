## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:f6291f585d119b58c0f6d7781457dd1bfa8e9c5765e50dfbdc9c800089372a51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:98a37369e1bbd613b0ed24ff9af3b5c0a512e6e640b04fa4a923f81656424bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256730643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37075f572b54e49eb0835233eda45abf599e5ca5ed68352ab29c03cb7cb85c8c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682f33f3678d0053de880087e1d2290f1d8ee653b89ee9c9c25c6ce2032a3b80`  
		Last Modified: Fri, 23 Aug 2024 20:04:25 GMT  
		Size: 158.6 MB (158579263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f45d787cec64c6f8cc8dd5a4a3b14e04c32a212d930f6fb3d396ea9c53e00d4`  
		Last Modified: Fri, 23 Aug 2024 20:04:24 GMT  
		Size: 69.0 MB (69024105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a6061e8bafa588b3c13ace13398078d71c5079713b34772d6f152f293dd385`  
		Last Modified: Fri, 23 Aug 2024 20:04:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa781b463c3fca6d01d817eaf6586ef05ae441cb556c96aa5e44aa78a89d3efa`  
		Last Modified: Fri, 23 Aug 2024 20:04:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6551a62018d7c3eb1fa48781c3348709ba37dce89866e619d1d35b69e5fce677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4762079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8ac4fd72a9fd1c2721e717cedd4e61d5959b3575e1a8415b29b3467abef2e8`

```dockerfile
```

-	Layers:
	-	`sha256:08bdb66fe343291d988c767490ae07e11f8843108e004042cbea14187b0353b4`  
		Last Modified: Fri, 23 Aug 2024 20:04:23 GMT  
		Size: 4.7 MB (4745870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a714f93c2af365815403c74989ecb6212af135da9e7e88ddbb17fcf9659d4d3`  
		Last Modified: Fri, 23 Aug 2024 20:04:23 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:96a9a098b1714eab7adc157a8013f260ce93a89330af9468c1a845208239cc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254677149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ba71b20128e7babefa2b58bee8e26b78ec6d103b9b4a9c3311c611c4d40973`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
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
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035a8666e0876988b4f21e47eefeb6a89566f18ce60f475ad21bc8119023c10f`  
		Last Modified: Sat, 17 Aug 2024 06:22:02 GMT  
		Size: 156.7 MB (156746222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6071fe6e44e43ab6156a28824131dc1a0d3725312a8471cf8d1a2f8d8cc94118`  
		Last Modified: Sat, 17 Aug 2024 06:28:29 GMT  
		Size: 68.8 MB (68773355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd443450f21aa2a69d02f7d30f1bdca30852cee7304aaa3766c3c9df99ae0d59`  
		Last Modified: Sat, 17 Aug 2024 06:28:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3a190dcf2c0fbb3351b251dae2eb295c24e3bd62e2c17079ddec7e2a52b374`  
		Last Modified: Sat, 17 Aug 2024 06:28:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5199937d250ab37247eec35f1cb7e191ba35903076b269f26616f1627a956574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4769053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebc922d045783314f4efd8af75b8e15ccd3a73cd8bf15fa21db3d0ae154e683`

```dockerfile
```

-	Layers:
	-	`sha256:024a012fcaa430b936ad317f8a3106ff36b804af3479a592c7be78a78533050d`  
		Last Modified: Sat, 17 Aug 2024 06:28:27 GMT  
		Size: 4.8 MB (4752279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eeb718364176b46f6f32c60f6b5a59eaaa3627ce99912adbf3a26fbeaad8b9c`  
		Last Modified: Sat, 17 Aug 2024 06:28:27 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json
