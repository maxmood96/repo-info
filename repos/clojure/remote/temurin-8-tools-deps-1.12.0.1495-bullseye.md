## `clojure:temurin-8-tools-deps-1.12.0.1495-bullseye`

```console
$ docker pull clojure@sha256:aa37b032d8bcab68ec442be7ff41d74a9cd9901c281301c24b512b53f13bec29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1495-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:812430fbf5d4fb3bf7de510c5a8a0e628bc710b8c508df28ebac0d21dc4e316e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177630000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7536c93ab6132cc1ce981308be0a90827b8fb29ee37bcf4f26c7b750c991c5b0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3689638af3b699d47fcea6328d27b18e7749c6523f46fdde93313afae0ac1d0b`  
		Last Modified: Wed, 22 Jan 2025 19:41:32 GMT  
		Size: 54.7 MB (54711736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a69d839b310f20218446fd8259af653b6dca2f791b290a38a3409ee1c8fb514`  
		Last Modified: Wed, 22 Jan 2025 19:41:32 GMT  
		Size: 69.2 MB (69178455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f95699de06177527f4231342dc59d398e122c8ef265b43f7107440ac07e695`  
		Last Modified: Wed, 22 Jan 2025 19:41:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1495-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:32b022785844e69ab6c932a629ff4ff2de9a6133365b9b73871aff8d29ac932f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7340402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0744f763175cc9d98536db44ada4907e4d6bc39a2655a0fa976e793f87fc7f11`

```dockerfile
```

-	Layers:
	-	`sha256:4fe8883162921206cb496b471bfd309d047712c191c533ae42b6d271680fba93`  
		Last Modified: Wed, 22 Jan 2025 19:41:32 GMT  
		Size: 7.3 MB (7326165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1c8e34d5346d8aabe2a67c3ef681bebeed704ff0918e4ef378ce6dbe067fbb5`  
		Last Modified: Wed, 22 Jan 2025 19:41:31 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1495-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78ae09bb42e501d081eeada137ffe149737bd8056fbe0d06d4c47e06b4762009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224298958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f0c41ea1c2895356410f1edd3a069e8ace33c1e34ae3dfeb36bee419e67d55`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f468498da49c43dd921b0f405aeeb87eb714221124b311e09a623dcaca2d6c`  
		Last Modified: Tue, 14 Jan 2025 12:15:14 GMT  
		Size: 102.7 MB (102747715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6817bdb8894774d6508b1a4657450732973b7097552ebc5b7bc0c48ac684ad4`  
		Last Modified: Tue, 14 Jan 2025 12:18:35 GMT  
		Size: 69.3 MB (69304538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc92b7f7ccca2923c202cae942f8ffe1919b64bba9e5da46f31b855dede5ede`  
		Last Modified: Tue, 14 Jan 2025 12:18:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1495-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5ad5ec67d8ada9b79f90ce14f0df1cae42ec622f22a6e5b82680ccfe01cd4b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7346932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af294e72efd6aa4258ad0868f8ffd322115e5abf914eaf05fb760d8fd3521b66`

```dockerfile
```

-	Layers:
	-	`sha256:dc5adca47148baa2651cd984e54eb8ac88f43cde75832220dcdc9e4dd1237518`  
		Last Modified: Tue, 14 Jan 2025 12:18:33 GMT  
		Size: 7.3 MB (7332572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3467456e73526610de8e14b69fb09278b81a423048c6fa522acf9e9f607d4dec`  
		Last Modified: Tue, 14 Jan 2025 12:18:33 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json
