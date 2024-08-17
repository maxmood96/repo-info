## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:1a213e94d372fb1633aa59c2dbd7fbffdf028f9a09daed8178ec4eed14a61856
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
$ docker pull clojure@sha256:001fc62c2192c8f0df8697cf50edcf1b9b65610b51ccac3a3f24a4ac6a50691a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191505619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91971b955b0ac3f01b9ec4a920e468f533277d0f5d33c135bec18c93fe31a6f0`
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
	-	`sha256:3cff1d0b1eb2e4ce5591d54e466446843f441c773beed9454537bf7b3d745679`  
		Last Modified: Tue, 13 Aug 2024 06:18:33 GMT  
		Size: 102.7 MB (102729219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85d45dcdc55d3a0f3d6f1209a6d04c21e802507409f8d8c64ae8fdfaa96756c`  
		Last Modified: Tue, 13 Aug 2024 06:21:49 GMT  
		Size: 58.7 MB (58699668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0dcbdc1354d05c73f7ca7a9e16a6e9bfeec673f7d558b7e630d441da718719`  
		Last Modified: Tue, 13 Aug 2024 06:21:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8f1a8cc7b65f5cf168609b1b204dcf84df3e4bdc97445af5e6213e4d96b66969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4996134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b75625860a570caf8cdbefee949b403bb673dea3aa10d07e09b2f15db78cd5`

```dockerfile
```

-	Layers:
	-	`sha256:a37ac97f807838e20c866aca90059e9bbf00e3478cb5c240db27205eabf3d4a0`  
		Last Modified: Tue, 13 Aug 2024 06:21:48 GMT  
		Size: 5.0 MB (4981673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cedd93f0eaeb403d516940dec0c136800fdea4f50b7f8a3d24f4eb4c6669ab6c`  
		Last Modified: Tue, 13 Aug 2024 06:21:47 GMT  
		Size: 14.5 KB (14461 bytes)  
		MIME: application/vnd.in-toto+json
