## `clojure:temurin-21-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:9156f06254e85998acf287594cdf8bc84a9ba987fbc2421ac39420ad8a0a567e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:199178b3e01aa58e9e356131ad36cebc08a7df9a08e0d1c7e4223d0b9d87e4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287060360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422959321589b2b88c5b8fc4b99af40596c6bd2e3427149c34c2a8e99cac0cd0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debc1dc56cde66ff720e4dea91acb24e97887ea4d7beccc0bced0a4c60a0bc4b`  
		Last Modified: Tue, 04 Feb 2025 17:11:57 GMT  
		Size: 157.6 MB (157585929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a401d16fa58598a0c0a9a5e949e084d4ca809ca685a611c2d122e1c578b97c02`  
		Last Modified: Tue, 04 Feb 2025 16:08:30 GMT  
		Size: 81.0 MB (80993703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2f1e55064adbdacc8acd7af4d4fcf6713f910cd91697efbe3a1b7d7a80ea3d`  
		Last Modified: Tue, 04 Feb 2025 19:12:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b5bb6b64ee0070a9e04b511f2ab3fbdf853158b716c106b52c03c9c8e0215e`  
		Last Modified: Tue, 04 Feb 2025 17:18:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:79d0b6904bc0dcf860c7736e0df870d902036937efae2e16c783b6037a631624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22a29f0e65054674bae787cca659d68efa4b6f79315a33b975dff5f0b1e07a2`

```dockerfile
```

-	Layers:
	-	`sha256:172232bdd6e321542ebf5763ca2aa1ce66cfeaa2c3bc6d3582bbda651c95270c`  
		Last Modified: Wed, 19 Feb 2025 21:53:34 GMT  
		Size: 7.2 MB (7176180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d5e43df7e3f8d126ef2b6722d519a1b60a3672c21668474f7141207ad1b85a`  
		Last Modified: Wed, 19 Feb 2025 21:53:33 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:71616f9667c364c6160585ba07f7ddc8bf498dcaf9a734b21d417882b89940a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (285012399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4a47087b6745eb9df1210f4b125f0228107cdfef57334ac1c7f139db650c94`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba5fa34edacd0f0acb63e2f1d258d50a9bfe6e1592d31c38031a099fd6fb4fd`  
		Last Modified: Wed, 05 Feb 2025 02:01:25 GMT  
		Size: 155.9 MB (155859274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaede25a02b77ee4efdf3c7ddf030786707abc2212e35e6153d6ff5acccbce7`  
		Last Modified: Thu, 06 Feb 2025 20:37:48 GMT  
		Size: 80.8 MB (80845530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a9f77e64a79e80eda2cd8a7f4677069b753eff3f220cf269c0d54574658e64`  
		Last Modified: Wed, 05 Feb 2025 10:01:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba965d7b9452451750c14ca8ba8301c3cd8d1eb276998c259ac8308457837b5`  
		Last Modified: Wed, 05 Feb 2025 10:01:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f295dd41c81b4137d3dc130eef5ddcaa7254e98c2166e9c005124d6db2c30754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01a4cebac0b9a20c1e394d1e3726fba6564afc14626f94ce0efcc84ec8fc3f5`

```dockerfile
```

-	Layers:
	-	`sha256:923eddecec3f98d863957b2b7484b75a95a42e9348fcd18b61255c1d57dc84cf`  
		Last Modified: Wed, 19 Feb 2025 21:53:34 GMT  
		Size: 7.2 MB (7182015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ae02a9b1e9da5db533830a9d4cb06c75e6e5fbf91c90792ba322edd24f691b`  
		Last Modified: Wed, 19 Feb 2025 21:53:34 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
