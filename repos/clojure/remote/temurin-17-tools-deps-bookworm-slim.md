## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:55e391d77502f6ba47c6901dab885f8ae95c0dfc515cda8d7e5a114b34feb62b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3bc92936527710376e4444e682139a441a972f79efb37e680498e7dea046b932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243321559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade1bf2ec201f6a80c30087c8d3004a139886bbb613b928468285836d81b2df5`
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
	-	`sha256:9abd4e4463045cd8d9e38d751d77499d5b9d3f7fe013d553db0b633d99394cdc`  
		Last Modified: Wed, 04 Sep 2024 23:07:52 GMT  
		Size: 145.2 MB (145166561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6caf8ac8de50fc85bdce92e0a711cb7e83e0e70df29ec49e82694defdf3a54`  
		Last Modified: Wed, 04 Sep 2024 23:07:52 GMT  
		Size: 69.0 MB (69027473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6874a894602a521f449a7a49043f810a2e6f33479cc1df2f8cc1f3240945cbc0`  
		Last Modified: Wed, 04 Sep 2024 23:07:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf4244edb971f9db84f0fe119d1832f4cbdb9bb4f25b87a3363b4c07a018699`  
		Last Modified: Wed, 04 Sep 2024 23:07:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:20cc08adc075e003c7f8744db2df2cec7a3b7cfcff939ae6e2783b7ddb30b6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4760676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07ca6c336e616051ad5167bf45cea24bf65ae548a7eeb38b0f0651a1462b687`

```dockerfile
```

-	Layers:
	-	`sha256:54b8250c9e893f6600092a3df1432d753b1e3b2e5bed871a74f28ba7f6ea8737`  
		Last Modified: Wed, 04 Sep 2024 23:07:51 GMT  
		Size: 4.7 MB (4745164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d96a5618bacafcbd13edc84595a9019975f4305379a35d34fa65dddfbc04984f`  
		Last Modified: Wed, 04 Sep 2024 23:07:50 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fdaaf91b8b943f6132062b83977814ccf9a47a1de1b8fc769a589db69b9f678e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241890495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeeb117d3406e1c622210e705521d214af56262cf1c931e0c19389f098154b07`
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
	-	`sha256:9363aa9440a1864d8f272d2e01b5da71ca2f092f5726a38615ddfb426b7339a2`  
		Last Modified: Fri, 23 Aug 2024 23:59:03 GMT  
		Size: 144.0 MB (143959466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef563227b4b17c3219494fff3f8b93f1e55b4e142d04462e0b3ab7a7799f9e9`  
		Last Modified: Sat, 24 Aug 2024 00:02:29 GMT  
		Size: 68.8 MB (68773454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b61266cadb78730a442e50af59c8a66fcdad081749245439d6bf4e6aab66f7`  
		Last Modified: Sat, 24 Aug 2024 00:02:27 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0f1901278a31ad5060a8d0d3128784f2b3c31f224a7b30aa53a865dd6c046f`  
		Last Modified: Sat, 24 Aug 2024 00:02:27 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:32d887fd171cc4a0a81a63c5666c7ca9975cb623746b12257109d9790a0f3188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4767603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24daac4faa81978e221b3dd23edc41cfb7ffc9ae73386b634b652b222e9e3bdb`

```dockerfile
```

-	Layers:
	-	`sha256:0673b56d086831adaa5a236ea0100e6a162fec960f6c62fb0493bb5f711661c1`  
		Last Modified: Sat, 24 Aug 2024 00:02:28 GMT  
		Size: 4.8 MB (4751549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23f56c2f475868d24af207ed2cbacc8bea59e89fa658f2d9351d0fda7be3732f`  
		Last Modified: Sat, 24 Aug 2024 00:02:27 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
