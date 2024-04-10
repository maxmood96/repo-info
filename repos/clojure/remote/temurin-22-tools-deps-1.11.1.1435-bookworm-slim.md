## `clojure:temurin-22-tools-deps-1.11.1.1435-bookworm-slim`

```console
$ docker pull clojure@sha256:43848829dae6f7cd412d5d2760dfa9eb06076317b7fd67ff9b6b90392b628ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `clojure:temurin-22-tools-deps-1.11.1.1435-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5a63580e3227bc764ca7ed3980a3231e5a4fca3ad468eb7e7a66c8c28e004561
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253842425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c820fe25dcd0cc71181b0f6ca30eae7636bdab2b9d9ae477baa91b1d9f7f90`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:38:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 18:10:36 GMT
COPY dir:804c07f15e876d329ef9551fe4e0597856a4396e905a8f833a1110ebfd35dfdc in /opt/java/openjdk 
# Wed, 10 Apr 2024 18:10:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 18:12:40 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 18:12:40 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 18:12:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -sLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 10 Apr 2024 18:12:56 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 18:12:57 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 18:12:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 18:12:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3086d6f8dfe5ce33e5286e773ecd6dca381e1af01152a5bba5f940cc50b168b2`  
		Last Modified: Wed, 10 Apr 2024 18:25:05 GMT  
		Size: 155.9 MB (155861747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c8cb91a1ae8b4dd83575829ab217aaeb1e3f7db274bff17953d9472ab21f9a`  
		Last Modified: Wed, 10 Apr 2024 18:26:44 GMT  
		Size: 68.8 MB (68817508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795c3f312535cd0e7e8feb4cda70433304308d1863785667b6fb6f3f2a77e5e2`  
		Last Modified: Wed, 10 Apr 2024 18:26:38 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef6786aeedd48ed18752d09e535e4c9dcd224971c1664ffca05ec253ed8b1eb`  
		Last Modified: Wed, 10 Apr 2024 18:26:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
