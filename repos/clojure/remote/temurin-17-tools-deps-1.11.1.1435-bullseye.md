## `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye`

```console
$ docker pull clojure@sha256:aefd857092fde0bbb51bec0f375f3ea86af6a9c7e2997d24f3d97d36fa2ddf06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:dffae7d39736aaa5f725e9ae529b48514745d8aeaba1c591eefc3360383a53b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268995284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2187f7eb5f1d1018a9b27eb9f1f1a146c30de5b29176a892058d8b0c77f905bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 14:11:09 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Wed, 06 Mar 2024 14:11:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:16:28 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 06 Mar 2024 14:16:28 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:16:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 06 Mar 2024 14:16:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 06 Mar 2024 14:16:47 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 14:16:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 14:16:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6eab155a0ed2d9028ca2f4a82935d930aace1dae36184ea7a85b71e3543e8f`  
		Last Modified: Wed, 06 Mar 2024 14:28:52 GMT  
		Size: 144.9 MB (144893105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c474e464a8c9ddf1bf99d7a094736c031738cfa8ea03282136dc29b3d6b7a275`  
		Last Modified: Wed, 06 Mar 2024 14:31:43 GMT  
		Size: 69.0 MB (69016323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3297683c84cf3675902f5fd3acecfa6dff4388851fcaebd19a0f27bfa805236`  
		Last Modified: Wed, 06 Mar 2024 14:31:35 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fe51bb7915441598b74db0c744e267df0834c5debd75cab34136d925946ce2`  
		Last Modified: Wed, 06 Mar 2024 14:31:35 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b7169b581f1d68493883f0eb0148a1b737e8486848a9cb6ce49b53464754a75d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266584906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f99318b2500cbb2d2669d4c1d9c86835294019fcb8534129d252100adba88b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 13:23:54 GMT
COPY dir:4a8c697909e89d854b955537d3c80fbcec33336dd00fb9805f3c0a9edf3861db in /opt/java/openjdk 
# Wed, 06 Mar 2024 13:23:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 13:28:26 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 06 Mar 2024 13:28:26 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 13:28:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 06 Mar 2024 13:28:41 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 06 Mar 2024 13:28:41 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 13:28:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 13:28:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6455a65bd6ad4d9673722258d4cd56d6bf8df5927f8fc237ec05a3773a3bfd50`  
		Last Modified: Wed, 06 Mar 2024 13:38:33 GMT  
		Size: 143.7 MB (143720835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57d437d32be3f57dbf69e74a566a3f4ab9dc3b0dc21c93209ef677d60b8549a`  
		Last Modified: Wed, 06 Mar 2024 13:41:06 GMT  
		Size: 69.1 MB (69141568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f2121f054f343cf8688c5680280e661c2edea29084407e55905bb5558b8b5c`  
		Last Modified: Wed, 06 Mar 2024 13:41:00 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0dfcbc91b467f44ff94ff8b040b27ca3cf4c5f76e75b1239c3c24a6d200495`  
		Last Modified: Wed, 06 Mar 2024 13:41:00 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
