## `clojure:temurin-25-bullseye-slim`

```console
$ docker pull clojure@sha256:27dceb1d9e80974f6b96b6c8aed67ef20100cf6c9e247d7a516a87a97de8b7e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6bb000c278c0aa8b10c620d7d570b7b9a2ea6533d3def7a826198203a3854821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181454790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277ac1c3caf1bf1ceb2f63974b4f52143ca4b1a373469ce83dc9015eb11c40e0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:40:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:40:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:40:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:40:27 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:40:27 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:40:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:40:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:40:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:40:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:40:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fb86543a3cf2c2117c591cc333441167f2b11c0600f906611a8868d585cd52`  
		Last Modified: Thu, 11 Dec 2025 22:41:17 GMT  
		Size: 92.0 MB (92045301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0ec4cae7c5a7dfd9a334ff229785a7ca5d126b043b324d90fffc1ad1c93c2b`  
		Last Modified: Thu, 11 Dec 2025 22:41:11 GMT  
		Size: 59.1 MB (59149986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bdc41019107aab47776271cc2f8cdd22e3945c0aa6d1e688624a6c0356bea8`  
		Last Modified: Thu, 11 Dec 2025 22:41:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ca0f5bbae22762318a7fd90fd6a52477f19d53f2391a89acacfb75ef1f6e64`  
		Last Modified: Thu, 11 Dec 2025 22:41:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1ab06669e15a73d30a5ff2d0e3a69416aaa13c1637b93b80f4a31868e382cc71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfc7b19f8f1356efb9b4dbad1df52ad0918313c98665f786635ec62f1cc81c4`

```dockerfile
```

-	Layers:
	-	`sha256:54920c091056d8815c6ac4ce30b1bb681420c20be2f4d79e7df195ca799c67cf`  
		Last Modified: Fri, 12 Dec 2025 01:44:22 GMT  
		Size: 5.3 MB (5259427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7820c988526ed3e0a17fa0d96f3ff5b8a6f44963c866e72eddcb536eeebca55b`  
		Last Modified: Fri, 12 Dec 2025 01:44:23 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:06354b73a474b93be0ee80fcc629faf830da427793d458cdbf28bdda1f65f866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179086476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5bfa3b91dd8794f6604fefb2ec27256f11f49195a9745cb1c2c72084075807`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:38:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:19 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:19 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:38:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:38:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:38:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:38:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:38:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f50b4991b03810c67ca2d3bccc99939e51a983b450c63d0310699a06fb3c588`  
		Last Modified: Thu, 11 Dec 2025 22:39:05 GMT  
		Size: 91.1 MB (91052481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8309733a4a39aa6d3d4f8fc97592d6514b0c6ecfad05116dba1a04ed5ca778`  
		Last Modified: Thu, 11 Dec 2025 22:39:04 GMT  
		Size: 59.3 MB (59284473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12bc2911dd97258333af30349ef528c65a3d30b53a36ab55ee9065dc7b4af72`  
		Last Modified: Thu, 11 Dec 2025 22:38:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f6dad100dea4c904574893142b7deeeb236629973ca6ed88efa3cd41d0be7f`  
		Last Modified: Thu, 11 Dec 2025 22:38:57 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5feb7962b7e494f69ca20739ba1513eee54cb35d42af61582a8bd7826c30207d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d73dd008cf17daebfe5259c2fb060a9d427ee5212356091b44c3cbc62277f9`

```dockerfile
```

-	Layers:
	-	`sha256:dd7bc8c2b6d565e998ea6c235ff16cd2c458e66fde126fca586135bf6a228e8b`  
		Last Modified: Fri, 12 Dec 2025 01:44:28 GMT  
		Size: 5.3 MB (5265180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06799c75018a29ad47160244674f268a452350b1d851f43b4ee77ec986ae1b18`  
		Last Modified: Fri, 12 Dec 2025 01:44:29 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json
