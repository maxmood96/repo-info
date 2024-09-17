## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:6754552649ebdc3c19f40dde95f5de8c931a5b73069d5808f6e8bb35f7357f07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:88602e042fe73be628597ae9834bc021bc501bec745d832c5277bc6415575a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (276036073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137006e7dd871d54ec2fc893cd760cadcf5ba73a62c71aecf99243b2d585e638`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7094dfcf768c2c008049104c2a1534c7f356c2867ac1ed542f7eb461be07ad11`  
		Last Modified: Tue, 17 Sep 2024 01:56:49 GMT  
		Size: 145.6 MB (145550046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e745fd0975aa63807090c397328f0953abf322cb23cbce20702d753e79a40bdc`  
		Last Modified: Tue, 17 Sep 2024 01:56:49 GMT  
		Size: 80.9 MB (80928678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27f89f4317aa05bd441fbb2c242c1075b433daf64ee57ce5479512889d51bf2`  
		Last Modified: Tue, 17 Sep 2024 01:56:47 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3d94f6351cbdda488d93b20f875f04c0ac821077a816bc26dc6b6ef2cacbd09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7020851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8596bfd96555a6102f4f68cf56c940b90b5acfe00dfde8b8862e5a94e3bf67`

```dockerfile
```

-	Layers:
	-	`sha256:53edd3d4edd5c2c1487496bd3d46dfa4b6aaac404af02ae8aec88cb49cdd4d32`  
		Last Modified: Tue, 17 Sep 2024 01:56:48 GMT  
		Size: 7.0 MB (7006987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02e09ac12b39f024bbe9a88a79ae26d9d12fe9faf48c452d66e87bc0d39a883c`  
		Last Modified: Tue, 17 Sep 2024 01:56:47 GMT  
		Size: 13.9 KB (13864 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7fa6008897cda9cc33613448761c08c1ed74309e26d9f88a5de7546992369f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272388553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc27447d76c8c672836092984df350f987f481e89a0eadc5c0406a507c77ccf`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393395a4d0c87c9bffae02a06bee32000ebf6954efeb8794bf23fefff730eb60`  
		Last Modified: Fri, 06 Sep 2024 21:10:13 GMT  
		Size: 142.4 MB (142354818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0b2d5e7b01fd0db416433dde37a55c7995c5266bb78ec700cf4dcea9ffe398`  
		Last Modified: Fri, 06 Sep 2024 21:15:14 GMT  
		Size: 80.4 MB (80447465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae5331fd0854d16c97efd010c51c62df8c97b9b4ff814f9285afad771479fdc`  
		Last Modified: Fri, 06 Sep 2024 21:15:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b270e51f6d84686299a383cab52ebd81cf56cc6ce56fed9f28abb38a05808149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7020259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ce2956f639b8b0daa897738e8ccd4e1026f36ec1edfd2ff3496b085a6b76be`

```dockerfile
```

-	Layers:
	-	`sha256:b4ba3bb0468276fd4e7e17e5fed3ed5862113f35802f5c9eb24dddf20a393fc2`  
		Last Modified: Fri, 06 Sep 2024 21:15:12 GMT  
		Size: 7.0 MB (7005858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f100dd00c7a6efbf0cb8587d18ffecf604c403fb7ec4f79e42f02c7b13af4175`  
		Last Modified: Fri, 06 Sep 2024 21:15:12 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json
