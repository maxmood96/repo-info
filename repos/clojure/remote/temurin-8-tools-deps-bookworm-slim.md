## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:3f87e0c0629d280d2995df90e4a3856cde9e1792bb3c545105d7b717bde17d9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3a192bfe483ad5964532ae6fcbf575dd6f12c767f711c61b4071bd2e7d9b4d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201763225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7cc6fac6d6913a4685daebd282ef03dfc2c0dc91324dea5edc5276e7c1febf3`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd8ab3175a54ae946d6dee0fae087560bdd280eeeb4eb7a0618522f60d5e98d`  
		Last Modified: Fri, 23 Aug 2024 20:02:00 GMT  
		Size: 103.6 MB (103611892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b92df603c6a872468880ac06d84199b1e503ab23dd99344df071829114fd0a4`  
		Last Modified: Fri, 23 Aug 2024 20:02:00 GMT  
		Size: 69.0 MB (69024455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d05d07a900fd7c7c0afbdf97d3b16695e5286c0cc80b28a63fe33ba4c57112`  
		Last Modified: Fri, 23 Aug 2024 20:01:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ef5591f59e5b63c1d547690da068b14dda8e83438160f6832c0edb21379f98f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4784576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b6cac046ed87b7bcd883f6fa87adb3cdbb5df7015eb6203264f16167e7c051`

```dockerfile
```

-	Layers:
	-	`sha256:f50d51dd61030380b4aaac091c078e3ad25ee72043dbf64661d38cd487f31c12`  
		Last Modified: Fri, 23 Aug 2024 20:01:59 GMT  
		Size: 4.8 MB (4770655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9a8fc62c39dad303fb6fbe9fcd5e46560443b73cff1e037832dafb4da79967`  
		Last Modified: Fri, 23 Aug 2024 20:01:59 GMT  
		Size: 13.9 KB (13921 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ea697214feffadcafa9b21a3687d198729eee40740827f1f1e7fc4fd0a1a9657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200659249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6debbb9706e90788023e1afe2b4084ddc26e47b122b731a2790a62c00e34240`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edcc7a7af68400eeaf570c17969676510119f264dd0e3c2e9727f01574ef515`  
		Last Modified: Sat, 17 Aug 2024 05:51:40 GMT  
		Size: 102.7 MB (102729220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3bead7a57dc0e19cb89ede2dd23bc3f99e00d3fdbc8029756ebeee42c77f26`  
		Last Modified: Sat, 17 Aug 2024 05:57:09 GMT  
		Size: 68.8 MB (68772855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac1d1084a3b9e944e3c1e469cf4fe436f24386887b751d633fc3514f45719e2`  
		Last Modified: Sat, 17 Aug 2024 05:57:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5ee945ce8a19c38ddfe2df4740d2e529a46f17e119749fd84daceadb7c0bc000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4791501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ce403f94581209794f4d67c6e20334b409436dfe7f7682e623dc135cd2df27`

```dockerfile
```

-	Layers:
	-	`sha256:4a2753663594de653db6f00dbaca61fd7fdc093d30cf41f127f0220649d6f953`  
		Last Modified: Fri, 23 Aug 2024 20:47:24 GMT  
		Size: 4.8 MB (4777040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:569cf0cc338e7087186074ef2754e7ef19c609fbd57d4403ca963bbbc385af68`  
		Last Modified: Fri, 23 Aug 2024 20:47:24 GMT  
		Size: 14.5 KB (14461 bytes)  
		MIME: application/vnd.in-toto+json
