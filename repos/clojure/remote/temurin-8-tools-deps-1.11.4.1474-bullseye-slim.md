## `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye-slim`

```console
$ docker pull clojure@sha256:29de20970f34768930790ed9f36146dc446a3741fee4d72bbb59fe77d3f6158e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:57bbde3027a6edd41bae84dd054045a109c78a0ffb8a3c8d7abe7638ee7d511e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193743527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0e0549c109ed5fb8cf6993723d63a762668554bd55eaddecae71114fac0038`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
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
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796d88936df3534647d9751435371448bb2c4b586a194ab524bc20613724ae40`  
		Last Modified: Wed, 04 Sep 2024 23:07:44 GMT  
		Size: 103.6 MB (103611899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56680e6154f0ece2375e3cfe7801001e8b903df87a56c96fb33d02dbb0bec870`  
		Last Modified: Wed, 04 Sep 2024 23:07:43 GMT  
		Size: 58.7 MB (58702306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e810ae8591aee1c6b7457a8ec3f4b22c6bcd5fd8a4d98e7ac4bee7b9cbe0264b`  
		Last Modified: Wed, 04 Sep 2024 23:07:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:72e647e8096de26e1734b066f6c23d3e687c9f859da89c06e1b0a350a2a637bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4989238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9348f795141b196527ebce54fd628bf597ba96c9a6966a6b466f8b1400c3a74d`

```dockerfile
```

-	Layers:
	-	`sha256:fa166e1fd80656715e5ff79d8ae99b11a59f6158f1d37bbdedcd71508cda4c21`  
		Last Modified: Wed, 04 Sep 2024 23:07:42 GMT  
		Size: 5.0 MB (4975317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f22f73b4a8348567b7cd94e5b5ecdc5df904e9ab0808abe12a052a99bbabbd5`  
		Last Modified: Wed, 04 Sep 2024 23:07:42 GMT  
		Size: 13.9 KB (13921 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b93ab45fad6bef38536c1589d71aacd607a5adee3678e1e2b97b2134eb57fca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191505651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91ff139674a4e639346821da86ad84570033c74bd84a3379131358cd754ef53`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
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
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb51859b870a1fb12b81d80a40fc8b349baf98ee32dc9205b1701fc6ba1ea395`  
		Last Modified: Sat, 17 Aug 2024 05:53:33 GMT  
		Size: 102.7 MB (102729220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f107d32853514815ec8e281201e01b5b74d6da5f5ab106e8ad9d0cf2e1517a2`  
		Last Modified: Sat, 17 Aug 2024 05:58:44 GMT  
		Size: 58.7 MB (58699698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818f8270c7375e3a1e2228a3176ba4259f4965ba1264a748515eb365d1b6e291`  
		Last Modified: Sat, 17 Aug 2024 05:58:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:356d18de3be51998acc6388256c1423ec80bdbf23df589c462579f21f97c5bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4996134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b832339afb98a2d71024e6ae5b89eded6f69fe8af50845c8b4cf3a82cda638ac`

```dockerfile
```

-	Layers:
	-	`sha256:7c7f4f1b42c375a305b144335bfcc8c5d27fadd6e676838c0225cc642d266a35`  
		Last Modified: Fri, 23 Aug 2024 20:48:23 GMT  
		Size: 5.0 MB (4981673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a14a13f4d245a0c6c28a1742dfad55fef153333c359743919bdc4539b97faece`  
		Last Modified: Fri, 23 Aug 2024 20:48:23 GMT  
		Size: 14.5 KB (14461 bytes)  
		MIME: application/vnd.in-toto+json
