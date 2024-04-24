## `clojure:temurin-22-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:b645ede6820bfe4708a5dcdc7616e6d43cc7f229f8d87713e91ed19860f8bd6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:537d9939c966d3ac0ab934ee727afa91230ea0fd74abda2dfe8206fb532c864a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.0 MB (281986490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7536d4e1d0d4ecaacb9599423a20ade088e0df2ed83db5e2e29974465b7b5854`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:18:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 20:35:10 GMT
COPY dir:657bb663bfeaa42d669fabe632e75f73eae3c4aa2d4e78ab7b29311c6e01254d in /opt/java/openjdk 
# Wed, 10 Apr 2024 20:35:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 20:37:34 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 20:37:34 GMT
WORKDIR /tmp
# Tue, 23 Apr 2024 23:37:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 23 Apr 2024 23:37:53 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 23 Apr 2024 23:37:53 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 23 Apr 2024 23:37:53 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 23 Apr 2024 23:37:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da2ffb94eca311d9c9101d8d150b1695770fe34c75056a7a977470658b6dfa5`  
		Last Modified: Wed, 10 Apr 2024 20:51:09 GMT  
		Size: 157.9 MB (157879828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624df4aad72cdefc47c853c74662dee3c0727c35b1ec009e4fe2707d64006fc4`  
		Last Modified: Tue, 23 Apr 2024 23:50:17 GMT  
		Size: 69.0 MB (69015379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c9eef0570664e3bd20571775a0a3a9c719c688acd6647c0917200c0cd5b892`  
		Last Modified: Tue, 23 Apr 2024 23:50:09 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bf9f053075d693b461b8004108490a72184f969626cb6b9f12e7878ecfb345`  
		Last Modified: Tue, 23 Apr 2024 23:50:09 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:93ae156d6a595533a0f888cd388ce2a5aa0eaf4920ff252f4da77447c35a26fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278733007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234edd027b1913a49991c24c571aac19969255d58dfa0697efc4a9306f684870`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 18:10:59 GMT
COPY dir:804c07f15e876d329ef9551fe4e0597856a4396e905a8f833a1110ebfd35dfdc in /opt/java/openjdk 
# Wed, 10 Apr 2024 18:11:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 18:12:59 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 18:12:59 GMT
WORKDIR /tmp
# Tue, 23 Apr 2024 23:50:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 23 Apr 2024 23:50:51 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 23 Apr 2024 23:50:51 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 23 Apr 2024 23:50:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 23 Apr 2024 23:50:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453e0e45824683f2713a59af9cbd4793284df183e3286817c53b364313825b61`  
		Last Modified: Wed, 10 Apr 2024 18:25:25 GMT  
		Size: 155.9 MB (155861708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0323273b2d4903eedb5b22f811ab871d1ce106a9bca97f5d95dd38d3f8dce49`  
		Last Modified: Wed, 24 Apr 2024 00:01:43 GMT  
		Size: 69.1 MB (69141103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d31bdd21e67656a2f5ed39da5e2076afee5e942fb83b05b3639236b468dffa9`  
		Last Modified: Wed, 24 Apr 2024 00:01:36 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1cce58763a3f92f69dca859a7f56dd8bf7b66d78f0a2e3ba423e8fb78eee2f`  
		Last Modified: Wed, 24 Apr 2024 00:01:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
