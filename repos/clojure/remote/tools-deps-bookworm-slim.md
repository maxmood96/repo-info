## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:56e4ec9900b440c54cbc0d6e67f49f38cf3a74442336ed634623926daf75a087
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a378069cbc3107e6fbbabca71e0f5e194a101a72763bb93062a22cd91c3603e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256734354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4587ad4033089802efe1c260a06f5946f7568ba20a710d8be18b229244f3c1ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
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
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823aeb8c3ab592d61954c6aa36a29665715ac32cac0e8870a3be86d4de427efe`  
		Last Modified: Wed, 04 Sep 2024 23:07:54 GMT  
		Size: 158.6 MB (158579196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce5cc616a9e9a8c7fd426d33cdb798f5a479addbcd78d3dda5e91a439167091`  
		Last Modified: Wed, 04 Sep 2024 23:07:53 GMT  
		Size: 69.0 MB (69027633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd939b15f4b9fcebeccb271cb420e7d77c009dbfb4a0ada56444d735fdefff47`  
		Last Modified: Wed, 04 Sep 2024 23:07:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134dc51aee997b14b1f2a06edf623bed15950145fbd35d44c3407ea2712d00c8`  
		Last Modified: Wed, 04 Sep 2024 23:07:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e974fe41f0022473e51bbd3fc229fb39e3a6466cacb8c3d841d9b1ca9e1dfa08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4762079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5feca594c6ecf2996c1886fbeec30db78e531916fafeb685ebd021564176cd7a`

```dockerfile
```

-	Layers:
	-	`sha256:6bc36fc7d23e43fac184b798e63900c4f84718f3441d8afbea362f698d2e9d42`  
		Last Modified: Wed, 04 Sep 2024 23:07:53 GMT  
		Size: 4.7 MB (4745870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01c831bb24bfd9a1a2a296bad0a86ff55ea2a7cd6539327949b1bd9fe232a80`  
		Last Modified: Wed, 04 Sep 2024 23:07:53 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:96a9a098b1714eab7adc157a8013f260ce93a89330af9468c1a845208239cc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254677149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ba71b20128e7babefa2b58bee8e26b78ec6d103b9b4a9c3311c611c4d40973`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
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
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035a8666e0876988b4f21e47eefeb6a89566f18ce60f475ad21bc8119023c10f`  
		Last Modified: Sat, 17 Aug 2024 06:22:02 GMT  
		Size: 156.7 MB (156746222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6071fe6e44e43ab6156a28824131dc1a0d3725312a8471cf8d1a2f8d8cc94118`  
		Last Modified: Sat, 17 Aug 2024 06:28:29 GMT  
		Size: 68.8 MB (68773355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd443450f21aa2a69d02f7d30f1bdca30852cee7304aaa3766c3c9df99ae0d59`  
		Last Modified: Sat, 17 Aug 2024 06:28:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3a190dcf2c0fbb3351b251dae2eb295c24e3bd62e2c17079ddec7e2a52b374`  
		Last Modified: Sat, 17 Aug 2024 06:28:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1a0743553d94a128506bea0377ed7d874b1ef79b930b31b0680cec1e3d07d0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4769053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f989d6c1dd20a3fbbb56ac37da00a652c441e83087b7235763124a82a6298d23`

```dockerfile
```

-	Layers:
	-	`sha256:3435b9821715fe1b0bdf2a8ae35311983ce47caa78d195a12c43f71b2d0b3fce`  
		Last Modified: Sat, 24 Aug 2024 00:06:55 GMT  
		Size: 4.8 MB (4752279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6451158a58b34119b36f2ed55914c0371791be01e3034952941fd65bd254ff39`  
		Last Modified: Sat, 24 Aug 2024 00:06:54 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json
