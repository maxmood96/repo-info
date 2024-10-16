## `clojure:temurin-23-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:6aa631ddb4605a574effc93b8f23a19e7422abc162cdaf5b1b5151e214402b66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9166d92ee53da73fec36ec0dbf766e279477b96d8abba04d09dcf48ae4e40b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255637167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76609960d722d72703565f645bd4216412a50fd6d0464c0273634198a4f0364`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a08fba2f57a75db49c1824818343a5b915b356ef63b3dd45685c4c43320b89e`  
		Last Modified: Sat, 12 Oct 2024 00:54:02 GMT  
		Size: 165.3 MB (165267575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d6829ecdcb4f420a339c7ff72011d8c5901aab70e371603c0b9ac88a234d26`  
		Last Modified: Sat, 12 Oct 2024 00:54:01 GMT  
		Size: 58.9 MB (58939950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804577b4894a4d425481e3a7f0048b3396eca2cc4d66e16f79ed1f10004c3eca`  
		Last Modified: Sat, 12 Oct 2024 00:54:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3b3182e2b419ec39c9394e1e59fc3dd0cfed740ba66ae8476f4cbe250917be`  
		Last Modified: Sat, 12 Oct 2024 00:54:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1a7f4c43edf4347485acbbc3822efa2a13b3f5636418126e07c7f8560e22b75b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be5834d310f28f3c76bd4f76ba590c83639b99e40287b5414f2f542d94884e8`

```dockerfile
```

-	Layers:
	-	`sha256:6f6e8f73674df2473651613ace736edf004445514f9f7a571bfbaa6dd9196c12`  
		Last Modified: Sat, 12 Oct 2024 00:54:00 GMT  
		Size: 5.1 MB (5104478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2463687df5a09be88744c91784c6ab621995e197a5bc35698b8c7937208e1778`  
		Last Modified: Sat, 12 Oct 2024 00:54:00 GMT  
		Size: 15.6 KB (15551 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9a84a9693c5726e9ee20f84e36a3cfd6e78ee619f9ee312ec0152e7836efe0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252402351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1214da1f33991d66650aedf844e890b81a607528aeb1655d43fff93054edc96`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e41c8aee46923b85d416154b4ad4adf86f1fe9e3faddd049e229c3bc3e0ba90`  
		Last Modified: Sat, 12 Oct 2024 01:35:12 GMT  
		Size: 163.3 MB (163252810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d442cf097cfd9a4571e3bf2ebdfe9006efcd005d2ce9601e9b0d6be49d61b9`  
		Last Modified: Sat, 12 Oct 2024 01:39:20 GMT  
		Size: 59.1 MB (59073340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163bab70ecc92a264a639b0109408a07b29796cde0695660d28be8d20498f1e2`  
		Last Modified: Sat, 12 Oct 2024 01:39:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb8a9a809495a9a3680d62546920075b2fd635f822e7d996f91b0b785bad748`  
		Last Modified: Sat, 12 Oct 2024 01:39:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6f31b815358ce2090c8fb7c08348ce78ddd2ba1df48c01b950aca9513a0f6594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de893aa254921ad874d01757c609a0896e7804d04046c4c004f75d69eb8de7c`

```dockerfile
```

-	Layers:
	-	`sha256:22a4c4a985df5fcbd54ca0b1f3d8a208a929473b93e3c080c666d6d566ca349c`  
		Last Modified: Wed, 16 Oct 2024 02:43:16 GMT  
		Size: 5.1 MB (5109593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c232b26c74dccfec0a9370b4922f647d66ae120f5a6076fb61199e42cc01a324`  
		Last Modified: Wed, 16 Oct 2024 02:43:16 GMT  
		Size: 15.7 KB (15657 bytes)  
		MIME: application/vnd.in-toto+json
