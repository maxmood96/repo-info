## `clojure:tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:852b0374f19f753721be7fbe22f70b7549caa30b0088161f7eabcfe997c32286
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:515189096ba6a2277f07d31f61bcc0acf7cd3a448904b354facccf59e844904f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255333748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b05e937c6d642447ee107367ecc1315929502c3ff17663af9e9b5b0332a8dd2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c8c4c6620f306c98bdc0ea9f9cff407dc796a9e455f81e60ccfb6b1de0580b`  
		Last Modified: Mon, 10 Mar 2025 17:40:17 GMT  
		Size: 157.6 MB (157585894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33d4e653ef64ec6a1a33fc373396d18ac070f9c09b7b603f1e41baab7a08038`  
		Last Modified: Mon, 10 Mar 2025 17:40:16 GMT  
		Size: 69.5 MB (69527511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759e30407c72bbf66d620d621254cd7ca039b607e7d7578acffeea7420b93664`  
		Last Modified: Mon, 10 Mar 2025 17:40:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbf72dca4915186a7d62840ea02ccecd22d40c2f77419a9b708a30a48915c93`  
		Last Modified: Mon, 10 Mar 2025 17:40:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5e5e6fb58ab91164d1d58f596574ee5c37ba9b7bd737de00518179f3c63ce1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc183397327df87ca68ccf71ff8e78b0dbb508bf99f46386d92672f68781312d`

```dockerfile
```

-	Layers:
	-	`sha256:597c10e4fd535324fb1a90364df89f25b02309ba32d521cc17728cd4be38a61f`  
		Last Modified: Mon, 10 Mar 2025 17:40:14 GMT  
		Size: 4.9 MB (4916383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b5a97f61c84543570a789597a20a4281d3b5ca657eea5e76b4f240244e761fe`  
		Last Modified: Mon, 10 Mar 2025 17:40:14 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:529f89015e8ada9700754ce233f531eda5a4d11cd77d1311af6d875158324554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.3 MB (253287649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfe4dff28571981d87039a88bbbd68d82f825ac192d83dd747e0ecaaf80ea73`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c2106d6a51f9b7ea4fe06b86169ea4e78dd5217d57185ad4df2b9116337371`  
		Last Modified: Mon, 10 Mar 2025 18:10:35 GMT  
		Size: 155.9 MB (155859274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ecf927daa41444e41f19af56fa94d2c4b87c52bc9fdb38c0abb38249d2f931`  
		Last Modified: Mon, 10 Mar 2025 18:10:32 GMT  
		Size: 69.4 MB (69378906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc135b3cbb2bc5e738ed53c946bf275e99a4993576cc04f3f3d0c0992b77272`  
		Last Modified: Mon, 10 Mar 2025 18:10:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f09864b574f6f22f079f014a3a60bc2791a4c0982b089329b27f93e2e7849`  
		Last Modified: Mon, 10 Mar 2025 18:10:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:392157b34ab50ef4a2ce7022ab53d765a1ae6531f949496a735ebdfd85f8c00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c588473bdc8f056c6a6bda8ee84f9477695da34adbfba5e5c513556a68793c75`

```dockerfile
```

-	Layers:
	-	`sha256:07343ace8da596183fcd9a912df0c7964107b1514f467b8313da87c69073d372`  
		Last Modified: Mon, 10 Mar 2025 18:10:30 GMT  
		Size: 4.9 MB (4922168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f0810080076fd58fa77d001098e8363f0a0479ed47428510b6708fb7cc97e1e`  
		Last Modified: Mon, 10 Mar 2025 18:10:29 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
