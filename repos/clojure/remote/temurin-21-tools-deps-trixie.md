## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:765ff0ba5f90494f06cdc331882c0c4e484325e37521f7de9ac3e4fdebd87237
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:1c0cf30e8a3168d92e317496e731e96516a7544988dabb0c2f9f4de231f27466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 MB (293074046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1988602ad6f6ce5a5e45a4a6dfa9d23afd992eb9c6ce7e28ae66de8e5fb2a3c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:15:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:15:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:15:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:15:32 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:15:32 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:15:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea298a53c9e20ec0239a76f1509245b920d7aa22ac80d38533509023c452135e`  
		Last Modified: Fri, 15 May 2026 20:16:14 GMT  
		Size: 158.2 MB (158166957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0359898917fac9e01be6dd66f3660701f6069f3126075846bdfcac54406056d7`  
		Last Modified: Fri, 15 May 2026 20:16:13 GMT  
		Size: 85.6 MB (85603726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a34d216cc95755c3e97df881cd5b5f84f3b75abd588a0c8c1db2ca74008dd4d`  
		Last Modified: Fri, 15 May 2026 20:16:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58fb5ab818603f53986945c6110aeff95f847b58bc2be7334f407ab4a0fbd0e`  
		Last Modified: Fri, 15 May 2026 20:16:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1e0cf3cd6cc53b380efbdc19b7b0de282cf777cd7ce422019497d5ddbf14e2ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49125953460ab656c11f411aef3509754d70bb5fc8adda419492f4bfd7da931`

```dockerfile
```

-	Layers:
	-	`sha256:a3d2d693feb253f86effdd4280f1b8102d7e13e61a49f094ec4c4af947ee55ee`  
		Last Modified: Fri, 15 May 2026 20:16:09 GMT  
		Size: 7.5 MB (7473234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d1ef442e92318cd1d16af7a424f222856a85e6305bb3b46b3f555f2ac5e6c0`  
		Last Modified: Fri, 15 May 2026 20:16:08 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:38f5aa85053a552a6495de37fc2d0b6fa417f9e0d8076d2bbaf66a9d3a8d05c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291547135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92318c6d2b27f48322495df2af1bcebc6444636d6014c2284a7f69abedb83413`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:15:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:15:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:15:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:15:26 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:15:26 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:15:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:44 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb40937973526c02aea50ca18e4ea4abd50400792418383331e7bf13b25013cf`  
		Last Modified: Fri, 15 May 2026 20:16:10 GMT  
		Size: 156.5 MB (156461329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a81f64e2ab691c70acaf34e4bde98edc05bd36c6a892aa2f5e3f38ab900e5df`  
		Last Modified: Fri, 15 May 2026 20:16:09 GMT  
		Size: 85.4 MB (85415319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6da3a6eba4d012d34ca6f1c2fcf7acfe58f457f92ec1f6238c399a1c5dec743`  
		Last Modified: Fri, 15 May 2026 20:16:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f3e35d0c083c37ddac898cd774111eeed21503a025bbb50918f4df3fd7449a`  
		Last Modified: Fri, 15 May 2026 20:16:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a30272e52687cc4ae00e95dfec4e157ac03ee9a9fcfa41c8ded99b7776596666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5e18c35676051f5342bd625958456abef4014bc60cf362a147de044f88bac8`

```dockerfile
```

-	Layers:
	-	`sha256:e2605a799a4587d44cde3e90e0d341e4e1afe2e649e0653d9ed6f7eb67ee5a12`  
		Last Modified: Fri, 15 May 2026 20:16:06 GMT  
		Size: 7.5 MB (7480264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:817cccf6d1a978febb9c0b19ae86f4b91179a71f54eb989d9087f5ddec2087d0`  
		Last Modified: Fri, 15 May 2026 20:16:04 GMT  
		Size: 16.0 KB (16025 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:3708f9dcca8477b129b4d5878dbc2ff83e645a9b0f95c7b37df3c7b1d063516c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302475333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3998e523f8cdd08d0c3b8e27e28ab577735d96b17724a5cbd9d48d4502fe8e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:37:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:37:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:37:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:37:56 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:37:56 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:29:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:29:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:29:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:29:50 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:29:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9429fc219825eaf2a233c26bd84cdc3eef77eb70dd8fad888800a28c7609e2e4`  
		Last Modified: Sat, 09 May 2026 02:39:07 GMT  
		Size: 158.3 MB (158343282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c92b5ad6742605627d2efa917595a8445b128353d4e9c3a0de8107f1355286a`  
		Last Modified: Fri, 15 May 2026 20:30:31 GMT  
		Size: 91.0 MB (91007844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fa0ae59bea57a9a771d61a1b4913ff9b02161ee79887648eeb33d3cdc4dcd3`  
		Last Modified: Fri, 15 May 2026 20:30:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935beca0eba42314e64327717881c1adb06ed766c8c7bcb82d5d87b1c7bf3c57`  
		Last Modified: Fri, 15 May 2026 20:30:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b55146ad7b53e9d4f442a29676cea844ba832f97740f12c6c35c340558f98ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162b1a558cd43ce0c519da9672c4c0776f6c71b587c3e343a0ce5cacfe172f71`

```dockerfile
```

-	Layers:
	-	`sha256:b7061d1d4792def69b8128fc678b36d1d4bd1a2f85d7eceacb3dabfe7cc4ce92`  
		Last Modified: Fri, 15 May 2026 20:30:29 GMT  
		Size: 7.5 MB (7477655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d147473ea16c8a3f1949cc3d924156d8873ae0a5f05299de9d32b4888eb22a`  
		Last Modified: Fri, 15 May 2026 20:30:29 GMT  
		Size: 15.0 KB (15000 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:1ab5b8087e0c10db45ceaa6c362a1ec9adf5b4db59e2aca8b30362a4033dcf1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.3 MB (283327779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c632483e81e9c231e5383aaa50e8ac4092767944cc732684b1246262ecd9a527`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:29:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:29:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:29:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:29:08 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:29:09 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:32:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:32:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:32:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:32:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:32:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba69f29607ee8398fcf2e41d643b51acd78862008b319c7e3e63e96b8c2eb047`  
		Last Modified: Fri, 15 May 2026 20:33:06 GMT  
		Size: 147.4 MB (147388346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6687d2b60d636b6a69e62afa9a39bda0746c0f808a98dc9451c8b0e4ae9ca18`  
		Last Modified: Fri, 15 May 2026 20:33:05 GMT  
		Size: 86.6 MB (86566082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289a8c68c7ae2d2eb10de5c937d4788461eb4aa08962a915442182c237fab2ed`  
		Last Modified: Fri, 15 May 2026 20:33:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58ea1c97b499c19bc089e9fc82bc7889cf2742ae478cf22f0d3cbf4ae72fdce`  
		Last Modified: Fri, 15 May 2026 20:33:00 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:120c9be933e65fe310e873cc8f623e24cbbf6fc73a8f81ef2f49f61bd9d52539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6062010ad7ee99ecc9212720aec4e0d7dc4803dc99a6aa2e1660105212379b2`

```dockerfile
```

-	Layers:
	-	`sha256:2b4ceed1e961a94d425bf6eeac4802b33a50d0d50506fd896e8f57a000a556d7`  
		Last Modified: Fri, 15 May 2026 20:33:01 GMT  
		Size: 7.5 MB (7469156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0502c3bed7a9cba5fbbecd49d681a0090d2c3264425eeb035074bb00b9c2a892`  
		Last Modified: Fri, 15 May 2026 20:33:00 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
