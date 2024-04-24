## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:60f760f9bbe6fc439260cb8d18d943f512f7e2dd3e8f9ddb8924b4bf3370c259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cd8252419d9fec26f2dad89d130502c77c108e05bddf44710fe9404bd121b435
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235156354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a832e4cffa68b15e9144ab534f370de2fe35f8f1b34a2f38d0640dd1e987f9f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:25:34 GMT
COPY dir:61bea833528044db01491107d8c3fb583322243082c7798fd60ade98f7eb7613 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:25:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:27:57 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:27:57 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:28:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:28:14 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:28:14 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:28:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:28:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7e18e44024b12fa79056e86f735c6c20697aa58245c774350b1e9ddca45558`  
		Last Modified: Wed, 24 Apr 2024 21:49:00 GMT  
		Size: 145.1 MB (145095322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded939b9a190a12b14ba517d77d633ef3d665f9ab6aec5279bb1ee5788ccf378`  
		Last Modified: Wed, 24 Apr 2024 21:50:46 GMT  
		Size: 58.6 MB (58625751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1c6f7132050f582dccd842cacdbd83e30933641e6ff799615882dbf73903cb`  
		Last Modified: Wed, 24 Apr 2024 21:50:38 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f052ce38c8da22720fe4796ea77787227c6bb9788082846c4b811dea547e249e`  
		Last Modified: Wed, 24 Apr 2024 21:50:39 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e4a657d241d617d5ac63bf0b1b472b3cb11e1820e426e64a99cc59085b5024f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232732222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08a1543891064e76d7623be83b3a8cf50aaabf6695e55869731b92468c38e77`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:09:57 GMT
COPY dir:894420f494a8d73ff0a7e5986ef0142218654b95343c81b2b9fc9a9d3ea0c174 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:10:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:11:55 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:11:55 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:12:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 19:12:09 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:12:10 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:12:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:12:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3254ac111733cd25bc460b2088616d0660016859ecaff8c9aaf6f761abfcc9`  
		Last Modified: Wed, 24 Apr 2024 19:29:09 GMT  
		Size: 143.9 MB (143891815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e0570291efc4f3492cba3146fb12e017845c32a130389d3f26cb3d07e196b4`  
		Last Modified: Wed, 24 Apr 2024 19:30:43 GMT  
		Size: 58.8 MB (58752053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c498a307d2884ff02377e2790c0b03de49815a26fc4cae48bcf15b6d41650215`  
		Last Modified: Wed, 24 Apr 2024 19:30:36 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c5d6ede1d9e4f62fe61d1159d96c04702d572ae7d08452bce5115ff9137a97`  
		Last Modified: Wed, 24 Apr 2024 19:30:36 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
