## `clojure:temurin-23-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:c66b87804a0ab0b3a6e6978ddc84061846e0304276c69060b351923d4b09aac1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b43f3658dfb5886773f172e7c84463f53d9aa82a15b751a8b4c5356e88937226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294790875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ecd8b3398c3c4aa6f4b45c16db60006610fb46df0a79e75de8e639fc6454ec3`
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
	-	`sha256:4842d7d6b0c6dac7c24a8e4aaad0151d3b693cd30df69e4f0e6c506cfe73f205`  
		Last Modified: Fri, 31 Jan 2025 02:18:34 GMT  
		Size: 165.3 MB (165316197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fc5d132698379e2bcbfe17a7b915b761b9b51d9419db2ed8a4acc40ecda084`  
		Last Modified: Fri, 31 Jan 2025 02:18:33 GMT  
		Size: 81.0 MB (80993678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5701b5817d2b974a11ea32381b75affa99f82338a8f5c5b686ba45d0726040`  
		Last Modified: Fri, 31 Jan 2025 02:18:32 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff9207feab209bd01fa1d105e1673e2a612464f13e80bb17d191d164a4af501`  
		Last Modified: Fri, 31 Jan 2025 02:18:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2d47302e63d057e67c732775232122eae8e338e9fb7f8bd08b716326e582bdc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5a211d6b348a5447e0263250c6a318b86eac2d3033bda26b23046cd9aa4c30`

```dockerfile
```

-	Layers:
	-	`sha256:1960377ab2235eab2ffb5f2e999dd379244f78e5f2f61be5b942c79a9636e3e6`  
		Last Modified: Fri, 31 Jan 2025 02:18:32 GMT  
		Size: 7.2 MB (7176767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f2d7c6b3dd86506ec156ba568306513c6a6c0759394bf3cac9ded812a76bfd`  
		Last Modified: Fri, 31 Jan 2025 02:18:32 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-23-tools-deps-bookworm` - unknown; unknown

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
