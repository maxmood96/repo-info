## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:b21d2de210ea5867be24a64f9145541ac2e29f088f1c2c516f22c42142054260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1d8f3936628b5294bd7c3e66d8067463012330cd4714686211a1ce9d1836a35f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243311958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa366b2511274b9ef1153207334bf26cbd57e5f83c5572a68a7f58ccc033363`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:24:45 GMT
COPY dir:61bea833528044db01491107d8c3fb583322243082c7798fd60ade98f7eb7613 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:24:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:27:12 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:27:12 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:27:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:27:30 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:27:30 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:27:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:27:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaf3a51e65fb5be60868458603f429cd0b008b781e06c9e52fbd6018557aac4`  
		Last Modified: Wed, 24 Apr 2024 21:48:20 GMT  
		Size: 145.1 MB (145095325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3018e22cb6dd8872d99643ebea9b8807cea955c736abd497bb20beca8fb0932e`  
		Last Modified: Wed, 24 Apr 2024 21:50:10 GMT  
		Size: 69.1 MB (69065136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36dab03f4e4b0180fe4c558cf18f3e029815cb1d437628fcd23d7a666e2aa79d`  
		Last Modified: Wed, 24 Apr 2024 21:50:02 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92df546a0a9fcce19f840bde2853c99a1bdaedf71fd59b50bf8978d59f0d5cab`  
		Last Modified: Wed, 24 Apr 2024 21:50:02 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e8b8f5b27eb07064d6514e4accef1bb543e60f2c375b5c0980dced955d92555b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241892453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb96847590e2aece827afa0d31d87bcf8809c68009a21663539ef4bc5b979bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:43:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:09:10 GMT
COPY dir:894420f494a8d73ff0a7e5986ef0142218654b95343c81b2b9fc9a9d3ea0c174 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:09:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:11:15 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:11:15 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:11:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 19:11:32 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:11:32 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:11:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:11:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760600a5e2889343637bf277e65d485b109927b87e8fcdc44cb39ef52ec19dd1`  
		Last Modified: Wed, 24 Apr 2024 19:28:33 GMT  
		Size: 143.9 MB (143891815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d135ae309c53aa052b0d63c59f149c4d230a5c70c452251a32ad43542cbdfc`  
		Last Modified: Wed, 24 Apr 2024 19:30:07 GMT  
		Size: 68.8 MB (68819685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2312fa8798a109a88a1ab35396ea97124598abe9e99a253426f01055d3156559`  
		Last Modified: Wed, 24 Apr 2024 19:30:00 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c140f8e227e0f47b24db8f7e9cb5e399b6f842378662bf32d1c41dacc3930bc0`  
		Last Modified: Wed, 24 Apr 2024 19:29:59 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
