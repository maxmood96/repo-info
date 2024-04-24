## `clojure:temurin-22-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:1d99f9f80a9279e1da93488f5f324ad7c54234244dd9d49be596234084102fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1c939778edafef50b80fc8821a1e1e4e9635406ff91e30481d31c3d181dc8858
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247932999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ccc2f6498dcdfd774095b0c676dcfa0b41ffc7676b010de11d36d57cf70dd0f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 20:35:39 GMT
COPY dir:657bb663bfeaa42d669fabe632e75f73eae3c4aa2d4e78ab7b29311c6e01254d in /opt/java/openjdk 
# Wed, 10 Apr 2024 20:35:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 20:37:55 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 20:37:55 GMT
WORKDIR /tmp
# Tue, 23 Apr 2024 23:38:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 23 Apr 2024 23:38:17 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 23 Apr 2024 23:38:17 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 23 Apr 2024 23:38:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 23 Apr 2024 23:38:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb85f29f304fa22263b6b0a8d22d25dc0f68c14b2e2ceb0bc910b104e36fd2f`  
		Last Modified: Wed, 10 Apr 2024 20:51:31 GMT  
		Size: 157.9 MB (157879798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2921a19bdb7fec30cea22ab4b9c25a66bc3a7138cb69374ce257b251c8637815`  
		Last Modified: Tue, 23 Apr 2024 23:50:34 GMT  
		Size: 58.6 MB (58624447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4cf005841baf327f8bccb8f16278e8934e9b6e8328fa7a76c1429632b99ceb`  
		Last Modified: Tue, 23 Apr 2024 23:50:27 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e263421a03189a4d541c7400cf79bc266cb4a61d74a9d48b3c17ef9b6f45fcff`  
		Last Modified: Tue, 23 Apr 2024 23:50:27 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:054d0d11e608779baddec3490a2449ee7517c0c0cf289a13a45f0ba3d43117b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244689892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa937c781a6e37b72acdfe2da48d4eb1145e81fe864f907c0c470bad8ff7efca`
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
# Tue, 23 Apr 2024 23:51:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 23 Apr 2024 23:51:10 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 23 Apr 2024 23:51:11 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 23 Apr 2024 23:51:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 23 Apr 2024 23:51:11 GMT
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
	-	`sha256:387e0775fc34184f00d2ee7190a9a8071e2e784db08bcd96e4b69aba9886a3a9`  
		Last Modified: Wed, 24 Apr 2024 00:01:58 GMT  
		Size: 58.8 MB (58750820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178341bbc69474abf9a347fe49200a42b17fe762a2aa163d3f8fac49e587e487`  
		Last Modified: Wed, 24 Apr 2024 00:01:52 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18aed72c1a6b454614178d661aa6c3a25ef4a5f391197b7abdfce420856cfca`  
		Last Modified: Wed, 24 Apr 2024 00:01:52 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
