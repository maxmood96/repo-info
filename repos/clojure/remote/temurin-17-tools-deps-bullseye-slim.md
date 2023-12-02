## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:b20e6837a2c09e69deb92f037e1f99c576991549b84f7e944c3c7124c10b313c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:624581871e021c4040eb2092aa172f6be6909bb48aa96c7fcc971828947930d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 MB (237796457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a444a7cbc7e940b49e4d6829742679c7f57c38e5b145f3eed7ec550611035bb6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 07:35:48 GMT
COPY dir:e13dbcd57950f4d4d23f4aba8428b6fbbf838d8f4801d32a25e344d37d33c37e in /opt/java/openjdk 
# Sat, 02 Dec 2023 10:03:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 10:08:12 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Sat, 02 Dec 2023 10:08:12 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 10:08:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 02 Dec 2023 10:08:29 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 02 Dec 2023 10:08:29 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Sat, 02 Dec 2023 10:08:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 02 Dec 2023 10:08:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4929994d0853caabbfd68ce7ab07e3af7c0e483db2f66881247df513f25c95`  
		Last Modified: Sat, 02 Dec 2023 07:40:56 GMT  
		Size: 144.9 MB (144873901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfb07f530cbb7e507eefddbed789fa9d788bb4f696775a187b7c91b055d2d2a`  
		Last Modified: Sat, 02 Dec 2023 10:21:54 GMT  
		Size: 61.5 MB (61503714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c772e0012414019805e462f44e52e4682fa880809ee5d273f09dc0ec647eb4`  
		Last Modified: Sat, 02 Dec 2023 10:21:46 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca6d0c998472afee8184880e731bb1a0c70de25ed19ca3fa3b41f2271eccf43`  
		Last Modified: Sat, 02 Dec 2023 10:21:47 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2e43f7e6e9002eed975f82aea088eeedf96a171d19723f599a25f1329b0c6dfa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235368062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d65cdf5fe4601916637728f8d23ab561e7287103771d8f4a7e2715e626fcc43`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:54:33 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Sat, 02 Dec 2023 08:54:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 08:58:48 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Sat, 02 Dec 2023 08:58:49 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 08:59:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 02 Dec 2023 08:59:03 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 02 Dec 2023 08:59:03 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Sat, 02 Dec 2023 08:59:04 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 02 Dec 2023 08:59:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d93fb72555944d51d7e18e85dbba1405725af6fa11dc155f20ab3dc455df52`  
		Last Modified: Sat, 02 Dec 2023 09:08:50 GMT  
		Size: 143.7 MB (143681749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecc0a762cedd1d790493ed440de7d990036f7894ab3c4307a474e5223a4a72c`  
		Last Modified: Sat, 02 Dec 2023 09:11:28 GMT  
		Size: 61.6 MB (61621171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360d762cde7a8843fd8798d373846e9cf103f5d7b139d88e6ea8de98a4edf6fa`  
		Last Modified: Sat, 02 Dec 2023 09:11:22 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb62d51a7b1d50aba61d6507b38475ab6ad847942bcb45e27cd07510be8ad33`  
		Last Modified: Sat, 02 Dec 2023 09:11:23 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
