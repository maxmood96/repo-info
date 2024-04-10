## `clojure:temurin-22-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:ab579753f7f8e856f39315533dc71c52a53f5f52ff5557da3aaaef4bc9265ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `clojure:temurin-22-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d730bc278a509c12e18a744bc384abcf941c4dc543eac398d8dfaf9d5c7737ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244689854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec2c9052cc739e4b635679d0734acb691b682f2145690b6c7d75e2350069e16`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 18:11:23 GMT
COPY dir:804c07f15e876d329ef9551fe4e0597856a4396e905a8f833a1110ebfd35dfdc in /opt/java/openjdk 
# Wed, 10 Apr 2024 18:11:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 18:13:19 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 18:13:19 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 18:13:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -sLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 10 Apr 2024 18:13:34 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 18:13:35 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 18:13:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 18:13:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f35cc8eec2bace08f7db46957ff7156dda89bb3618178e4f0e85a889f582c8`  
		Last Modified: Wed, 10 Apr 2024 18:25:44 GMT  
		Size: 155.9 MB (155861747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3bde9b9d69378a55e09d654b37fc1baa76bdcc8ff08fa4c39ade00e7cc2860f`  
		Last Modified: Wed, 10 Apr 2024 18:27:19 GMT  
		Size: 58.8 MB (58750783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6564da244bba595c336893e588cb750d8956fc5e99219b41dde612059da7ddb7`  
		Last Modified: Wed, 10 Apr 2024 18:27:14 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86f0f595a44236680f2836bad6724aa5e98e506838542d9e6c9c4315952cfe3`  
		Last Modified: Wed, 10 Apr 2024 18:27:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
