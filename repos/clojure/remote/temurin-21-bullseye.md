## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:b54067408990d2e44a8a77718b13bd5c33095e3434a6cf732453e8a371a1a429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a62ba4561541c8f4822bf576b89de5139e2d0ad4d6df828b73a7d71f548c8ad8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283660414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef25488e77f33bc523f38e292c0ac8da0f90a6df435a3cd1160bedba4f1466f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 00:00:14 GMT
COPY dir:64a8841762a9afbd2fb8b4cf497b2dee87765737d44ff0387ce1cfc51371c9a2 in /opt/java/openjdk 
# Thu, 01 Feb 2024 00:00:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 00:02:00 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 01 Feb 2024 00:02:00 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 00:02:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 01 Feb 2024 00:02:17 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 01 Feb 2024 00:02:17 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 00:02:17 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 00:02:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac4333b9c256cced06955a88cefbfd9b93fd1b42569f9c2ebda324bd77f6513`  
		Last Modified: Thu, 01 Feb 2024 00:16:25 GMT  
		Size: 159.6 MB (159582940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4fac71c5d990b48d7827fe5507bb92d1fe8df74cbd8fd92ca6de72b5e1125`  
		Last Modified: Thu, 01 Feb 2024 00:18:10 GMT  
		Size: 69.0 MB (69019491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3eff28f445fce3d1a165f412d9cc289d634c48fae079682b89ed3a446d40f0`  
		Last Modified: Thu, 01 Feb 2024 00:18:02 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f5e72b842e835ac3a0de6ba392d74bbb3480ee36c504356157c2941de359b2`  
		Last Modified: Thu, 01 Feb 2024 00:18:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:130a8df16da90cb272ebfd32121c8cf976a7ecde48fe72782c979da129756183
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280646056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad38f65ffddebd046f924bfef1b12aa55453fb6716e5c9dd2a4f46f4e1e9869`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:35:03 GMT
COPY dir:ab40534e435f9942975c0e8b5454d6b7a8d69c445f8e0758c1bd9c500e157fca in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:35:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:36:30 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 01 Feb 2024 06:36:30 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:36:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 01 Feb 2024 06:36:45 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 01 Feb 2024 06:36:45 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 06:36:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 06:36:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62cba91c04c8fb9fc51183c28a4bf7b61017854f51fbeceeb6d5042d36b85ab`  
		Last Modified: Thu, 01 Feb 2024 06:49:29 GMT  
		Size: 157.8 MB (157784601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc127f04fb896ff42313d2b1a27331e47d97bb5e9ea18b1150e29b1420de23c`  
		Last Modified: Thu, 01 Feb 2024 06:51:09 GMT  
		Size: 69.2 MB (69152171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa83916c9617dd75c8cff90c314ec0e70dec53b4a56eae828e3fa9196aac82c1`  
		Last Modified: Thu, 01 Feb 2024 06:51:01 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e107e99df0bd792df8419a384c508034e8fc534bfa4ca1411bc49171c32633f`  
		Last Modified: Thu, 01 Feb 2024 06:51:01 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
