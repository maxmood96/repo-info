## `clojure:tools-deps-bookworm`

```console
$ docker pull clojure@sha256:7215d5349cc0879143f76fdb985cd2aabceaa42a645fb42959550ff63eb9f737
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:8ed42660f6b19a16e43ec0fc8ea014d0a34fb72ce23e837f8beb741b49987118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288588307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82902bebc360fde32c55c6ae9a26cd5b54cf5d0ec68d4ca962e0042de094ca25`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af52aeeb81c491e394288d1a59b8844b05928b279413e8a0523792eb34ff32bd`  
		Last Modified: Sat, 17 Aug 2024 02:01:12 GMT  
		Size: 158.6 MB (158579306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692ed2c2eb0be57e75da476dbfa0b1befabeb63dc21a53a4942650231162792e`  
		Last Modified: Sat, 17 Aug 2024 02:01:10 GMT  
		Size: 80.5 MB (80453880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd70d93ef8c3ba8ff9a113dba7f5c6694b38bb77f79c2faf418b4fde55262d7`  
		Last Modified: Sat, 17 Aug 2024 02:01:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d51d1e143f912371bccb3bbf7570bd1a7cf9edff35ce8d0fe0d3cbb8d258cf1`  
		Last Modified: Sat, 17 Aug 2024 02:01:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:284ffc56264ec5abc8f325652dda0ed656e0e9cdebcc90b07b2dfbc6c0459e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7256f3652ca3fa4a3e801c85f5fed8ddd5a74351ec88d4ece0afe9c8568f8ca2`

```dockerfile
```

-	Layers:
	-	`sha256:b2811f10d295b724e499a5db1b8cba8481807c6e61efd4ed097c109d22fe7fcc`  
		Last Modified: Sat, 17 Aug 2024 02:01:08 GMT  
		Size: 7.0 MB (7002096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:029f43e44fbcd757444520028f3d3492789c53883226894c272d9bac53ea246f`  
		Last Modified: Sat, 17 Aug 2024 02:01:07 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:55872abbe0d7f005bd075238d7ca5a0d3de2e9c081f78d8d2f2d2cd6c67cb00b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286534231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fa53cf4cddb67ed2723607192ca7c0cda270f782fb31bef95dc84eb365024c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432a3dfe48f41ad044efed0a39ddc56c9ff96bfad23f28032c6b72e9206318e9`  
		Last Modified: Sat, 17 Aug 2024 05:49:36 GMT  
		Size: 156.7 MB (156746222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301280ba1adf4535e95ff22a9db87b681705d89c4c0cdd26e2078423d991a907`  
		Last Modified: Sat, 17 Aug 2024 06:27:44 GMT  
		Size: 80.2 MB (80198376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64123b6e5cb94e7d4c6b74dae2b5df37e555030f3c1915d1f418a848ca2e6b8f`  
		Last Modified: Sat, 17 Aug 2024 06:27:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088c75c54295a45aa171276ab10a28dca4194302447e81da3a4e02d5dc40478f`  
		Last Modified: Sat, 17 Aug 2024 06:27:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:81467e2dafef6a2f53fdeb653923d91184fde1083e0193ae69d2a6eea45b359a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7026603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08b571df6a619ed3ed22a95db2069754b9089d504af870a1dbc76538f11b428`

```dockerfile
```

-	Layers:
	-	`sha256:3ddf4d02776a0a9e3e74a098076886b5fe1b49e9e99c0b7bf0a90889f683e7a8`  
		Last Modified: Sat, 17 Aug 2024 06:27:42 GMT  
		Size: 7.0 MB (7008555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aefe5ef89bcca2be5e70cfc0fa32a20f966b41a3b20a60bca6985f5c79b3921`  
		Last Modified: Sat, 17 Aug 2024 06:27:41 GMT  
		Size: 18.0 KB (18048 bytes)  
		MIME: application/vnd.in-toto+json
