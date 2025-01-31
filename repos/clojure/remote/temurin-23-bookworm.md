## `clojure:temurin-23-bookworm`

```console
$ docker pull clojure@sha256:f13415afc888004ad404dcbc26c18e7aa7fa080262a9fc14e67bcbc8b128116a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:148dcf8f7f9509addac5b117d176538ddcda83aa9fbb1809f3329f6b0a732914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294770077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3dda8bb55c05f8ffb36a8054d9f8981418a6f18ee8418e92b1ceb6843ec1f24`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ae33fa43e3748bb10c39d2d5cab702e69ddeea59e4206f8ab72beb9249584b`  
		Last Modified: Wed, 29 Jan 2025 20:27:44 GMT  
		Size: 165.3 MB (165295053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de7a29b52cb5ebfb9078675849e7f2cd398f53462167201d43e7f165bbfa9bf`  
		Last Modified: Wed, 29 Jan 2025 20:27:43 GMT  
		Size: 81.0 MB (80994020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b01fe6c918f2fd795ad1e02136f4c980c2cfcaabc99e806dd0f6fa56ab050df`  
		Last Modified: Wed, 29 Jan 2025 20:27:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352f569ed637a1866165409779e0445fcc3d2be7018d6bbc58bb8c1a73485830`  
		Last Modified: Wed, 29 Jan 2025 20:27:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a14e77ba9d1bef3c540cd74a02c24d2f6b0f199d95b2356f7fea61a86e44155a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af095e9874b5e0abdf4e39e7d67fac51f701e76aa58f8fe257bd779504ef2ce8`

```dockerfile
```

-	Layers:
	-	`sha256:cf90f8120dd8c1d1d7462936abbf34f4565e74c5c1f2e5712103c3199a44ff01`  
		Last Modified: Wed, 29 Jan 2025 20:27:42 GMT  
		Size: 7.2 MB (7176769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66f42c56c0ad2bea086d78800c586ae89d42e7d726ee65c56639cee729c7fbea`  
		Last Modified: Wed, 29 Jan 2025 20:27:42 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c8a39f9b9b5f7b036d97e7498647cfb1ebfd82a54662df4f04abe0ac9d2bdc08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292435127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ff8d594a6884ba43dece46c2f910d622eee57554129e4d598b1e5955c1a5ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebbf68effac48458d835fb306b89c32b356ec1a36dac9070e972dcdaa0c8dfc`  
		Last Modified: Thu, 23 Jan 2025 03:53:51 GMT  
		Size: 163.3 MB (163281805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccec49f482a26c026e55442ae5852f51a57488e72c77ee9f30f58bde8e5c9`  
		Last Modified: Wed, 29 Jan 2025 20:57:40 GMT  
		Size: 80.8 MB (80845386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b76d328867cfedf46574e59967a78b21d1c8e7be2f9e4565447b69570739498`  
		Last Modified: Wed, 29 Jan 2025 20:57:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd08c57291ca6e84ebd5bfb4275f5a5188072995163bd6021b202ce8b842a99`  
		Last Modified: Wed, 29 Jan 2025 20:57:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9b6968c588a14353a4c8fd5eaaeca247da9d6e5c86b766a7b0eb504bbd35573b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf514c65e9c16df90d41dcf25fcebd9d873ef14168031581deeba0b922af594a`

```dockerfile
```

-	Layers:
	-	`sha256:4e8264bfe765b8a05ff295c9ddd3456b0d8e2b80275ea5c0c7701fbae2641ada`  
		Last Modified: Wed, 29 Jan 2025 20:57:38 GMT  
		Size: 7.2 MB (7181935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a2e025db38a9208b072c3fdf3680d36220b2a3d1e44be7dc00489e8431e9faf`  
		Last Modified: Wed, 29 Jan 2025 20:57:37 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json
