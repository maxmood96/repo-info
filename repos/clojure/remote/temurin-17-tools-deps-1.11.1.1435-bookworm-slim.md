## `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm-slim`

```console
$ docker pull clojure@sha256:0fa53a1548fc578eb0baf93531110df8ba944f660269295fc7f70e3c1c23c915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:67cf4740b58bd45e5970065e2b706aa0f718b4e879e08ca8a23a55feed60b935
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243080190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d796ed8bc86477310db163f1be4fe7b7692db130020f8d7f43d93586fa54e061`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 14:10:35 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Wed, 06 Mar 2024 14:10:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:16:04 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 06 Mar 2024 14:16:04 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:16:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 06 Mar 2024 14:16:23 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 06 Mar 2024 14:16:23 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 14:16:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 14:16:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44496d713a839fdd0b47c7b0973155ed9bb317b54231c21b7337e12eb724bb83`  
		Last Modified: Wed, 06 Mar 2024 14:28:32 GMT  
		Size: 144.9 MB (144893104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385d073a4a431a985558ae0c2080d4fa0384788d9dbd1464bd372dddde7842be`  
		Last Modified: Wed, 06 Mar 2024 14:31:25 GMT  
		Size: 69.1 MB (69061978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbffd67a8ff609bf2906cd420b3cbbfd3d01df8603570a13071396680ddf51b0`  
		Last Modified: Wed, 06 Mar 2024 14:31:16 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d1726e441b493417e36302da30188a4f5f8f0f091df332619da27742ce3b0d`  
		Last Modified: Wed, 06 Mar 2024 14:31:16 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1d6c1a86da3700edc87b43a758583e6f88db0538731fa36d8d856c49000a3af9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241695447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e35e885ba3bd346b5c47ff663661bb296f33843e8d6311a9f70dce32dac3c17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 13:23:20 GMT
COPY dir:4a8c697909e89d854b955537d3c80fbcec33336dd00fb9805f3c0a9edf3861db in /opt/java/openjdk 
# Wed, 06 Mar 2024 13:23:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 13:28:06 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 06 Mar 2024 13:28:06 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 13:28:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 06 Mar 2024 13:28:22 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 06 Mar 2024 13:28:22 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 13:28:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 13:28:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8baf922fb4d908d3a3587a0482690306454d53960171f76f1db75d33164d944b`  
		Last Modified: Wed, 06 Mar 2024 13:38:15 GMT  
		Size: 143.7 MB (143720843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7340a79d220a71a0af1c5a0f9a9acc695624854516ce388d5159512b1d13339d`  
		Last Modified: Wed, 06 Mar 2024 13:40:50 GMT  
		Size: 68.8 MB (68817228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83d5042c367b8be722f2417f2b6534a96a684468294d9687cfdaa4500d2ef95`  
		Last Modified: Wed, 06 Mar 2024 13:40:44 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f83a3a1ab75598f11a594a59c44fb263b4fda0cc71a57da237c4502ac38f066`  
		Last Modified: Wed, 06 Mar 2024 13:40:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
