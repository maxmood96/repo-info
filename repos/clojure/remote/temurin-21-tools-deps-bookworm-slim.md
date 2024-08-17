## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:1fd85935c2377445577da44ee540fe7e65bf93b1daf7c93d9257ba104a5be9cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bf3aa55bb1c762830dddb95c137563d4c6f0d200714a0f35e7dd201a1836d615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256730332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf50958383ff1385a69d0395db4bb75c385e48963eb4d7ea1027a4d7dfac44a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71410c4b6f060febfe7db18263b81ea634cd977319633e2e56c3830867e82223`  
		Last Modified: Sat, 17 Aug 2024 02:01:07 GMT  
		Size: 158.6 MB (158579249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c1f2e4416f595d1de26892b0307b8f531871216a23fe34d4c2656d0dd9a753`  
		Last Modified: Sat, 17 Aug 2024 02:01:04 GMT  
		Size: 69.0 MB (69023810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb41c80e339668928932e657db4495c99c6ff0d3e5f6f75d91c9efb599bb6b5`  
		Last Modified: Sat, 17 Aug 2024 02:01:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba334347aeb28f218797fdbdba82890dc1d2efe26ceb9a824fe5a277a2a1d0fd`  
		Last Modified: Sat, 17 Aug 2024 02:01:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f81171e4cf38527ad8703da36d1ea9f0f03e58334c3b66e44028cc89bff98e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4762079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfe2709db932f64153fb35b1cb240d8bfb6da2fea2baec88dae7ff071d346ec`

```dockerfile
```

-	Layers:
	-	`sha256:891ab779172549c7e0569c783122e38ee762c62994c9b456d4744b74a1620220`  
		Last Modified: Sat, 17 Aug 2024 02:01:02 GMT  
		Size: 4.7 MB (4745870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aa954bd412741149ca97b4875605b4bf44b79015d48c8709f895d16d8490273`  
		Last Modified: Sat, 17 Aug 2024 02:01:02 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:170893dd1cab3650d4b32067c13fc5b40b4ffe326809562de249322dd4913359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254676992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5390219465d0bd8b8484af8f784539ec91d01f79d9626ee97d5fd4fa53122b28`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9bdfd61932d57418e5a13a18609c024ef2d46c81b5c70ebc50602548d04c8d`  
		Last Modified: Tue, 13 Aug 2024 06:38:33 GMT  
		Size: 156.7 MB (156746174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca52845eaac1ee8ba025deda2fe4859ed4fcbfdd5bdd723a431eaee5c092d96a`  
		Last Modified: Tue, 13 Aug 2024 06:42:01 GMT  
		Size: 68.8 MB (68773253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6df2fb05450978ff8b5db7b06bbe9a934eaea543861ffb7b5ea1ef477b2c0f`  
		Last Modified: Tue, 13 Aug 2024 06:41:59 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce9cfbc75248328602e2809c71d85bc8328cffd8eca52b729fe13ad1ff16a41`  
		Last Modified: Tue, 13 Aug 2024 06:41:59 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d893a7d9d02ee25d1ae19a590117f84baf9e8875878c47008a8cf71a823fe6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4769053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d4d47811c24b177b52399a68676d9edd4834d51facfba983694fd8d2786510`

```dockerfile
```

-	Layers:
	-	`sha256:4590edb481c007bf824e97c93733c7582aa51be4d10c17f7e71918bdcf4d2eec`  
		Last Modified: Tue, 13 Aug 2024 06:41:59 GMT  
		Size: 4.8 MB (4752279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72a8214e23e5fb451f6162e56989dfc31a42a544fd1ff136e305ab360b1b6480`  
		Last Modified: Tue, 13 Aug 2024 06:41:59 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json
