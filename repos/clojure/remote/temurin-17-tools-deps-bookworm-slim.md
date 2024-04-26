## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:3b415c954932b343bb69783bbad84088c67e1386f91fb19080ff962b1a6ac011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3385d05a436b627e78e0fad8e6a1d2f2db465d4a0b4eebd8ce9a8910ed1b9dca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243313627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29b2cc934429c1aa6c506f524b6f4d65ed2db00378da621191eee9e4f1f8a37`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 04:48:42 GMT
COPY dir:36f5164517b1d083643fb66b5ce80f151a1fd45f701835f30c768c906e72895e in /opt/java/openjdk 
# Fri, 26 Apr 2024 04:48:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 04:51:01 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Fri, 26 Apr 2024 04:51:01 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 04:51:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Fri, 26 Apr 2024 04:51:20 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 26 Apr 2024 04:51:20 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 26 Apr 2024 04:51:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Apr 2024 04:51:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e618d306764ea59c5928223827cd70770af285ac9d962cd45874e048e1c209`  
		Last Modified: Fri, 26 Apr 2024 05:02:07 GMT  
		Size: 145.1 MB (145095358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2447b7637a5d70b2c8879eee99eca42809cc615a641d284247c9969ad3646a89`  
		Last Modified: Fri, 26 Apr 2024 05:03:46 GMT  
		Size: 69.1 MB (69066770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e7f785d0fd2b5117b543a2d7c18ca419136ca92cc3644d38dc2d3bb81c2010`  
		Last Modified: Fri, 26 Apr 2024 05:03:38 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37586ff387636a39c9a420f4479c9155929a936c9b63c0deb59b0e1d0d1d86df`  
		Last Modified: Fri, 26 Apr 2024 05:03:38 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d6d0e794b3b08806abaac56f0d6ad4964a5340a16ace3be277cf080a822dd384
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241890492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2631ef297f674916240510fa83334bd4ea2ea2c9f79c1951fdfa2747fbc55b42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:43:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 01:30:40 GMT
COPY dir:c133644f5c07e30ba622e3ac6570b28080cd19be78bf4af55cfe492de2f59b24 in /opt/java/openjdk 
# Fri, 26 Apr 2024 01:30:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 01:32:49 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Fri, 26 Apr 2024 01:32:49 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 01:33:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Fri, 26 Apr 2024 01:33:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 26 Apr 2024 01:33:05 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 26 Apr 2024 01:33:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Apr 2024 01:33:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6770cdeed59ae538d00e090e043e138bd2d6efa9cbea2d2e2ed4018b891f51c`  
		Last Modified: Fri, 26 Apr 2024 01:42:11 GMT  
		Size: 143.9 MB (143891890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf2566096993cd179be62f2266fe65ae5c000c98c0668b07eb0b5e47750e0bb`  
		Last Modified: Fri, 26 Apr 2024 01:43:52 GMT  
		Size: 68.8 MB (68817651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3fd3b00804fbcff825aeab9a85e605f0fd477c57c892251f2da9554d21f7ca`  
		Last Modified: Fri, 26 Apr 2024 01:43:46 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a876174ea41dabf2320189ef97c7b136d646a8199fde34fe88fda33a919e68b8`  
		Last Modified: Fri, 26 Apr 2024 01:43:46 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
