## `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm`

```console
$ docker pull clojure@sha256:fe7838aa32af96c67b5ff0a417bd7cd5892285bab8a2b3c442568369ca8af392
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:bab1d51ac9dca4d56083fa44d003f47d01708f1dde598481e799a9decb6a9a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275075585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6926a023e70cf8e0d5b39d5e3138a5f46277bb4d9c94ada9624168ef97bcc5dc`
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
	-	`sha256:9c783511fd64e8cf6d1280cd0f3c01300b0f90fed62afe6b24248859008e71a9`  
		Last Modified: Wed, 29 Jan 2025 20:27:42 GMT  
		Size: 145.6 MB (145601458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f35590a30faba34c65579ee631bfc0fe936eb0785aa8a6b9ab59d89e59453c`  
		Last Modified: Wed, 29 Jan 2025 20:27:41 GMT  
		Size: 81.0 MB (80993520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863519e1793e16cc197fde5da892bfdb63b0eece7a20277c53b8445e20dd6092`  
		Last Modified: Wed, 29 Jan 2025 20:27:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b3743a9de58d8884d99dfa4b426802fe32a015bf0423df72be920cf9f5ad01b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00637827c9bd1412b8e947345186bf129aae55ecd1632ea55e6d4fd500bd52e`

```dockerfile
```

-	Layers:
	-	`sha256:caba449890b2a93d0210560f512624c08307a1cf84bdeb8e9f4b365fd0c1af4a`  
		Last Modified: Wed, 29 Jan 2025 20:27:39 GMT  
		Size: 7.2 MB (7191219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bfc54669918657880bbb699f54b2a625972eb6e49870c0f23fcf41f1fca0a70`  
		Last Modified: Wed, 29 Jan 2025 20:27:38 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3b9033ba8099d39a4ed495de568e432fb05a3f6aebb2a076826d7ffee6ac6cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271542775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b3c392579f155f5b8288f2cc1a0d57697cff3fdc36f6e74c3d945e2d463f7b`
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
	-	`sha256:1157dd9b6249641ddcda5672c01d7e5ba16f1f6e2738d00add4bde5e0f5fe98f`  
		Last Modified: Thu, 23 Jan 2025 02:34:52 GMT  
		Size: 142.4 MB (142389489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c1ef4d7c322c5e182402b9dd50d93a010b3e4f2f39bdcb4060c1b8f6a99f2b`  
		Last Modified: Wed, 29 Jan 2025 20:43:30 GMT  
		Size: 80.8 MB (80845745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea12019604872aa85e968a950b93dc36171ad94f93454465c2c61cb6ecb97a5b`  
		Last Modified: Wed, 29 Jan 2025 20:43:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a3656aae255d9d552cde633ae5ec2bd4ff188f75cd603735d8b1a2afd2199fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196c6d4075865a539185c88b1f8aa3324a06f98d07b8acab7132f7af6ecfe140`

```dockerfile
```

-	Layers:
	-	`sha256:01e298ab12b617be2cc0ad3c46e85b992ad5c875ddd03677c689a5590a6e52de`  
		Last Modified: Wed, 29 Jan 2025 20:43:27 GMT  
		Size: 7.2 MB (7197600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84a0dd9b00e5b07f7f6e2c1cde8cc5379d91796725bfe1d31e2970924be7e390`  
		Last Modified: Wed, 29 Jan 2025 20:43:27 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
