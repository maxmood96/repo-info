## `clojure:temurin-8-tools-deps-1.12.0.1495-bookworm-slim`

```console
$ docker pull clojure@sha256:24115176e5f2e3e8dbfc9c257d2d3dc2c5354d6ec776f059688642029d77653a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1495-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2ce70c85ad17a6775e8718b0ee33332e53777006d59b5c1efb32d1888204d58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152451297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9f07a188f87006f2c02dd7a3bc7a0dd30ff850e8bf2c2790f30e1d9a70b1ae`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d66a3e6f11a991c8bcfb09a85fea173739d463b17747bf44f4b63687ab39906`  
		Last Modified: Wed, 22 Jan 2025 19:41:37 GMT  
		Size: 54.7 MB (54711757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44d24947f56b339438b8b482013811273f5f5c497e0b0200698ed7a793517f6`  
		Last Modified: Wed, 22 Jan 2025 19:41:38 GMT  
		Size: 69.5 MB (69526482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413baa9e9441252fcdb77cf4d2950a4cdb3e1fe41d5815703f652a12c2b35f51`  
		Last Modified: Wed, 22 Jan 2025 19:41:36 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1495-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:de6008a70d4b54af0f3ce52b1bc9a1cc1e607ffdfdaefab96292b3b35199d32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5048468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0079c9c5cb2455e114f70bdfca6bddcf417a9e6c3f202470e4dacde819eed75`

```dockerfile
```

-	Layers:
	-	`sha256:37f37056eaaef6ab722f46de2dc8274978eaa66674f56b6380001bd625c787a1`  
		Last Modified: Wed, 22 Jan 2025 19:41:36 GMT  
		Size: 5.0 MB (5034177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75a07d8eac05857e1db1070050f070dd1a91fc0003d440cb99d51e5aa143a694`  
		Last Modified: Wed, 22 Jan 2025 19:41:36 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1495-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:43a1868cb8affa34ef16257f23d47e3dd85ce4d530bef6b81573508772370b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151232410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccb49139d486c60f2f9ea06e8fb5bc2f59121cbdc377bf67158ab6606bd6640`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ed982e50b4bdb3d1279aa12d665dff931239bde8ac859554117a355d2b785c`  
		Last Modified: Thu, 23 Jan 2025 02:25:58 GMT  
		Size: 53.8 MB (53816412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54060a27baf23fc2c556776ac2b76fe5bb06fe441555cebb84e9acade3cc8a4`  
		Last Modified: Thu, 23 Jan 2025 02:30:59 GMT  
		Size: 69.4 MB (69374322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041b63dab40609206909845bb47371ff53e8d31cd935a68a9bffcefc6f3c4d14`  
		Last Modified: Thu, 23 Jan 2025 02:30:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1495-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1dd301c9735b77566b4795408ae3649e56718869258ad90128ec9d53ade62785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c58aef1c5c795c9c2cce19b436715827635d8e1fbe8e2172acb8d2ee7ab4ac`

```dockerfile
```

-	Layers:
	-	`sha256:295d188adf59f9f93768733f2ca9504de5381458de3793e97a8cffb6bddba72b`  
		Last Modified: Thu, 23 Jan 2025 02:30:57 GMT  
		Size: 5.0 MB (5040636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d2f977cb0e5a3cfcc620cd2d7ae00ec2736b2c2932ca77a0b0aad58fe224ed3`  
		Last Modified: Thu, 23 Jan 2025 02:30:57 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
