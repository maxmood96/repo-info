## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:c60beb8904d8c2b8803358a189ed6152ac1bcb7b4fe4db63c001fbe32714aec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5405d556db0af42eb3a743dd460dec181aec5efc28d801eed7382397c5445229
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243079766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bca930f02b3db3b5a17e3072b0552822da9617edc3da0521e410bd05a77bc1a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 05:21:53 GMT
COPY dir:6673b976fb9ccd391df2de00f5738789bfa84c9bc068b98b869cb1d7436fd333 in /opt/java/openjdk 
# Fri, 16 Feb 2024 05:21:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 05:26:35 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 16 Feb 2024 05:26:35 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 05:26:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 16 Feb 2024 05:26:54 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 16 Feb 2024 05:26:54 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 16 Feb 2024 05:26:54 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Feb 2024 05:26:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954503457635d4984fa02d42e6a7fe96adb6ed04ec63bd42b5805de30d4f95ba`  
		Last Modified: Fri, 16 Feb 2024 05:36:46 GMT  
		Size: 144.9 MB (144892562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fd27ed3d8ebdd6996f33f0a68ce6d56f93c170ca31a5c4acf545188ad4ba07`  
		Last Modified: Fri, 16 Feb 2024 05:39:14 GMT  
		Size: 69.1 MB (69062098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ddfa6d8111c4c3302899cc018a8258ddf7e5a6880940cc4207a160d60e7cfe`  
		Last Modified: Fri, 16 Feb 2024 05:39:06 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b98c19d13eaf615c6315145ea82ce61d9203b88cb6cfe5b853bc61050298a0`  
		Last Modified: Fri, 16 Feb 2024 05:39:05 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0fe3bc18df194c38db431a2105eb179b56f199e8e2a276dedba09aee5b4ec93d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241695535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6d34d4778b39ea1ad1356226e1838c192dcfd0aa7d6751e352929d19d4a9d3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:05:02 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:05:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:08:15 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 13 Feb 2024 02:08:15 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:08:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Feb 2024 02:08:30 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Feb 2024 02:08:30 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:08:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:08:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fb8e9ed56ae2fc55656e8fa8952cbea195e103052380154edd3fd24c87552b`  
		Last Modified: Tue, 13 Feb 2024 02:20:52 GMT  
		Size: 143.7 MB (143720877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1af0206f782f899e8321783a890ef7e154333c31474b38ad3fced33b270648`  
		Last Modified: Tue, 13 Feb 2024 02:22:54 GMT  
		Size: 68.8 MB (68817281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db9e31a798b59bb39705fb7a52af99b00b985b8c9ba48c92c4b30c385b2736e`  
		Last Modified: Tue, 13 Feb 2024 02:22:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfce1d1317f1c1e6e38d5fb39ac5b49a5b18c430ebaebbbaa59080ab4ca78a9`  
		Last Modified: Tue, 13 Feb 2024 02:22:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
