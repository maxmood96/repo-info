## `clojure:temurin-17-tools-deps-1.12.5.1645-bullseye`

```console
$ docker pull clojure@sha256:7799eda2cce2c0162dfc1161a34a03604f11da9b802a941f664cb72f93abf6fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.5.1645-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1f4d34c102599366de0779c297c16b9c52528e2caafb536ab20b4a9360f7eae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269277362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2603d31cd3ee96df9fdb7ff5685f6c9dca074b4643173bbcad780176479b9a0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:59:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:59:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:59:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:59:00 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:59:00 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:59:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:59:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:59:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:59:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:59:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25276be76f8b323a07ffbe31e37a40863691263b93454f9fe6a78509566d54a4`  
		Last Modified: Tue, 19 May 2026 23:59:38 GMT  
		Size: 145.9 MB (145905444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e394756c90aad41e12d38f4c1c8d8cf305af983d4dca02675e07930de42559b3`  
		Last Modified: Tue, 19 May 2026 23:59:37 GMT  
		Size: 69.6 MB (69602023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eb8aebdcdfca1f28d50dadf5dcd40256723537251d30a2e6ecca5c80fe9f16`  
		Last Modified: Tue, 19 May 2026 23:59:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f31da9fbf1deec4600c6e3dd5defbffe2ffdad3cd3062922ddb8fe7451e785`  
		Last Modified: Tue, 19 May 2026 23:59:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1645-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:49b94804620c8ddeff5c48a58eb56ace9f055b070af845f713973d570cdffb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7424210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10823dbca57a3aacfefcb303f997f9f38909c49f100d2f4e394d4b2580cef0dd`

```dockerfile
```

-	Layers:
	-	`sha256:e60980352749380eadbf2e0aae62a4beecc5e9763e1c9f46f1a7a5e79d24530c`  
		Last Modified: Tue, 19 May 2026 23:59:34 GMT  
		Size: 7.4 MB (7408278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa7f5d91bad5c7533b8fbf10fd83a1c75c8dfda9a10b4550c82f75381c490abd`  
		Last Modified: Tue, 19 May 2026 23:59:34 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1645-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4837674678886c4c9dcd43e6f8c28beacc3eaafa5f70ced000af7c84d4808646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266753007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998cce73b0649db8b0be03f77e927a2319a2b0888483daa0db680b155c78f6b9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:06:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:06:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:06:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:06:18 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:06:18 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:06:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:06:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:06:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:06:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:06:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa1f0d121ecbbd0afff63b02ef21204d89b0c66084b9a33291a8e376dc6997f`  
		Last Modified: Wed, 20 May 2026 00:06:56 GMT  
		Size: 144.7 MB (144724358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b3654b8dbe33efcc908ee47e621d588e46625ca5acd6cc6aed2c33c085cbe0`  
		Last Modified: Wed, 20 May 2026 00:06:55 GMT  
		Size: 69.8 MB (69771028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a2a233a62eef4f7d6724a7b6e8566cc2c6066260d1308f5c8c64334a8358f9`  
		Last Modified: Wed, 20 May 2026 00:06:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529c06b7bd7426a604857a397d16d97cc895fa980ffde1608708790e5c318340`  
		Last Modified: Wed, 20 May 2026 00:06:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1645-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1533cf50c0eb8099d94cf931cd0ad230564561637b21e33e843808f90ae884bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7429427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3763b1b48dc1373e233d5a84b346dc6c9985018ba96b48625832f96f8f94ae61`

```dockerfile
```

-	Layers:
	-	`sha256:1531ed925bcd7e8f3692ed8992380722997015fa2cc83e805796ae684a5e6816`  
		Last Modified: Wed, 20 May 2026 00:06:53 GMT  
		Size: 7.4 MB (7413377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f15b1f2fadc1fdc110d256e531f73ac258a0990f4640fe2d8d6641f7fa5c1397`  
		Last Modified: Wed, 20 May 2026 00:06:52 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
