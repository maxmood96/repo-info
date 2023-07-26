## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:74675ad436289911015b3458612a49eaae235ec51989392315dd564648187bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:57e3074a2c8d9cb06e3b1d0e90e7394832ce28e21c0913937baa3b1c037ab892
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237743699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7082cec6f0f704ff478619549e707ea23b61319270921b40161fcb915df923d4`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:00:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Jul 2023 02:41:34 GMT
COPY dir:2fc258758bb2c25982e4c8348cffe5a1ab54f4c54e52ff852a817cdf5bd62215 in /opt/java/openjdk 
# Wed, 26 Jul 2023 02:41:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 02:45:18 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Wed, 26 Jul 2023 02:45:18 GMT
WORKDIR /tmp
# Wed, 26 Jul 2023 02:45:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 26 Jul 2023 02:45:34 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 26 Jul 2023 02:45:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa296f85e8a5f317fe3db90e195052dc2c98dd3fc543e75e5298a95ac40599f`  
		Last Modified: Wed, 26 Jul 2023 02:49:21 GMT  
		Size: 144.8 MB (144829554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a996593f0b649c1ee22b56726ed3fdbea014fbf8beccbbe48a8afe1cdeccdb28`  
		Last Modified: Wed, 26 Jul 2023 02:51:31 GMT  
		Size: 61.5 MB (61496141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db5c6769b69eb0ae1520df9e337afc8c4ea9ebe84e87ce455cf2f71d59627cb`  
		Last Modified: Wed, 26 Jul 2023 02:51:24 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ff82690ec4555ca8552d3c17f09c09ad27d8ba35bbbcb0ef2d0f4b78782b5617
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233243832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1cf8647f8771eb197d5a8d0a84ba41e5aaf084574fb7b2f78b45e4522c1caf`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Jul 2023 01:07:37 GMT
COPY dir:e71da8247d58ed4b0dfbf219951c863c79ac94b7f45cb60320ea827dfa699275 in /opt/java/openjdk 
# Wed, 26 Jul 2023 01:07:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:10:41 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Wed, 26 Jul 2023 01:10:41 GMT
WORKDIR /tmp
# Wed, 26 Jul 2023 01:10:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 26 Jul 2023 01:10:56 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 26 Jul 2023 01:10:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9764bfc347c8d9f94a13dbe1948f4a4e50fef24a4e1e5730fab2710cb583db8`  
		Last Modified: Wed, 26 Jul 2023 01:13:46 GMT  
		Size: 141.6 MB (141565338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64c62e61096e5a67caac170de0bfb135d06e31af79f239907ad60c21824e92`  
		Last Modified: Wed, 26 Jul 2023 01:15:24 GMT  
		Size: 61.6 MB (61614922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e61b559aaee6b44bd0bff22f90eaa08a8b11a995341665926fb9712808ad78`  
		Last Modified: Wed, 26 Jul 2023 01:15:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
