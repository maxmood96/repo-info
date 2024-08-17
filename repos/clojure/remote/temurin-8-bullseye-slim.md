## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:e0da627a09631ee8bff8cb585c4f9304e303a7f6393a2c4b06665892fbe5cf39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9473af4cb006084007409e547b91151263e1c2ebbd18e55a4b42b5aec430737d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193612716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b07bb88c5460372524af6aa3b41761f482141199b6194232cda54bd84a0b76`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
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
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf90f70fe554576fda812392c6671fa6a188ad651df1c9c87449b5b688ddc17`  
		Last Modified: Sat, 17 Aug 2024 01:59:24 GMT  
		Size: 103.6 MB (103611899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc36b9e131345ca422dcb97eb9df5c4b84d7f213036327f32864d811c0296a6`  
		Last Modified: Sat, 17 Aug 2024 01:59:23 GMT  
		Size: 58.6 MB (58571886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94893688a4a9b55955fcefa003278820f1c6a3eebf317bad7d1a0da228b90266`  
		Last Modified: Sat, 17 Aug 2024 01:59:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:21ddd4c0db7369bbc3e0c1b4d7f6bd481e463976e28a4a12ee4ce79518b81e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4989238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead27a69d8f38869453553b51e58dabbde70001430d0ed511833cf59da8fa513`

```dockerfile
```

-	Layers:
	-	`sha256:b3c2d5cec2a8ce17fa29b6d5825a89d9e08b52e036e5bb57312ceedf6b43b8f1`  
		Last Modified: Sat, 17 Aug 2024 01:59:22 GMT  
		Size: 5.0 MB (4975317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860a66d7bbfa1f3e0c3a38084dd2b9ad1e30b6d6d157f2989a3e9dfb0567dbf3`  
		Last Modified: Sat, 17 Aug 2024 01:59:22 GMT  
		Size: 13.9 KB (13921 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

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

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f92e6dbae90e9b16f8fef843cc14663b0fce8267548085a6df540ab01b26e45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4996133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba94b09d99c15711d76fadf27a045e0bec81deb755cc9f83456733f279eb52c5`

```dockerfile
```

-	Layers:
	-	`sha256:0e49923167cad52b11e4f3a6e5a011af67fc0fbb00a1e57615633536bd7a1c7d`  
		Last Modified: Sat, 17 Aug 2024 05:58:42 GMT  
		Size: 5.0 MB (4981673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad92000f34e23a7ebe56a6a17853b6f636c87aec01f515f61f413d23cad9c792`  
		Last Modified: Sat, 17 Aug 2024 05:58:41 GMT  
		Size: 14.5 KB (14460 bytes)  
		MIME: application/vnd.in-toto+json
