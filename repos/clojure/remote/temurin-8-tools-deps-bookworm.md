## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:e033b97a93a2887565bd6e9421679920d43443ba485e36555647650033b97be6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:40f38976f3471976d7bb40b72634e1a1373a2428fd44c34de3b871bdf2ea1402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184186103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40098b4d285648ee6a1002ffb6efacf775d8cb126cbdad3218d4bf40dcc4c9c9`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad4774e68675654b00b28a4d7f777776cfe81421b52596d210be924ff811991`  
		Last Modified: Wed, 29 Jan 2025 20:27:23 GMT  
		Size: 54.7 MB (54711738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e80d75f0b1a707ff7b312deb7ea3134326939710494f12d9605751c120263a1`  
		Last Modified: Wed, 29 Jan 2025 20:27:24 GMT  
		Size: 81.0 MB (80993760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb623d1d881f2ae64f432458a1343533c98c7396974fb78fc281c9c91a1cef7b`  
		Last Modified: Wed, 29 Jan 2025 20:27:23 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bd56d1804dfc639bfc1e3491ae62b23bbbf9a576bdfb6363d4e0c7de2b8dd6fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7306925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7497a1b8a24527526f6b308c676e992991d30e4fc102ee06e8fe94fa22055c27`

```dockerfile
```

-	Layers:
	-	`sha256:17f3f8002ea9df27e037dac5bcda943bf9ee8220cb9591229c0aa5943ace165b`  
		Last Modified: Wed, 29 Jan 2025 20:27:23 GMT  
		Size: 7.3 MB (7292688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e9df393e93a4d9c148a97ade813a112aacc43aab3ab6cca6f4bbdf94280abe2`  
		Last Modified: Wed, 29 Jan 2025 20:27:23 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3c9d6e47421f369134b53cd86de36dee42628141110ed7df5e1408d8dccaa385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182969585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d22b520e9d80c7f1c3b1fbda1458e5fc0ca097cdf58cdff91007a980b8393f3`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee6e7e7404e5fee83e19aa34b8768a574ebe6ad47bb0cd7533ca8f441d20965`  
		Last Modified: Thu, 23 Jan 2025 02:25:11 GMT  
		Size: 53.8 MB (53816418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40db327841aff0076118d062db2caca77684f14a79998777a3f86c0bf16045fc`  
		Last Modified: Wed, 29 Jan 2025 20:37:47 GMT  
		Size: 80.8 MB (80845626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b54df546d2ab0039d10f4f89ff35735407301141cca9678bdd546478fa8ff0f`  
		Last Modified: Wed, 29 Jan 2025 20:37:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:53d159c603110134fd39366ddfc464d570a6c5196553e3a7d81cfb8bfdf688b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7313504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042b11f82471e09f51c21934ccc20fb9ddc8200a2b606f67c268357a7052d942`

```dockerfile
```

-	Layers:
	-	`sha256:84cc136eca26d10f8933db3d961363a3acbe038089d8c3e9336516ee880424db`  
		Last Modified: Wed, 29 Jan 2025 20:37:45 GMT  
		Size: 7.3 MB (7299149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11ec160cdca37c6b6082772b0e339c507e47f3b9376d3c666e7f1c8c61291f8f`  
		Last Modified: Wed, 29 Jan 2025 20:37:44 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
