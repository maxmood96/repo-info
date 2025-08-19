## `clojure:temurin-17-tools-deps-1.12.1.1561-bookworm`

```console
$ docker pull clojure@sha256:966fa69f96ba43dbf27258182bfdeb16f33737ae4b5cd93e08abcc8e4b72b303
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

### `clojure:temurin-17-tools-deps-1.12.1.1561-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:182213b6198050108de87c08b1e9d4b20902d177ac21ac36d205e4b7ebde6c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274231524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4f77f5173143d59c840463c97d39060a6c77df21206175473c07759349535b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9154bb2fcecec024623df7a003982e4c136819dc4bdf86c9a64ae98f80145a3`  
		Last Modified: Tue, 19 Aug 2025 03:51:18 GMT  
		Size: 144.7 MB (144693301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542a8ab9249ff6d8213981db19b16fa4f225a192e1b81a6d877ea7d3159b2843`  
		Last Modified: Tue, 19 Aug 2025 03:51:16 GMT  
		Size: 81.0 MB (81042675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df95c31f08c39676e5852f8243b018582ab0a656b7a667ffeed8c99454486e01`  
		Last Modified: Mon, 18 Aug 2025 17:09:00 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1fe1ad00942070ac296db09d77895bc9cd24ae007188a0a34e70c52f3624df`  
		Last Modified: Mon, 18 Aug 2025 17:09:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1561-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:562f26ea26ee3490d7dae26972344742f41a2f968901a1873eda9f927de8352c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7384117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e48d0c87ec870886e5b034cf9a74e874e2cfd88789179f24342db1ac4d17805`

```dockerfile
```

-	Layers:
	-	`sha256:ab20926d535ce9fb557e3892cf908aff8ff69f55a7ad70c06dc43002b2f8c5da`  
		Last Modified: Mon, 18 Aug 2025 18:37:16 GMT  
		Size: 7.4 MB (7368297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db135440a7e1221c4d5deeb4d0a96322fcb5f42d77ae6d053e87ee9f0800c77`  
		Last Modified: Mon, 18 Aug 2025 18:37:17 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1561-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8d65bdb839cbaec280c27ef8e24a0ce23ae4e96d85e989758e0278a0bc33455b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272799230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52dd27ebf25a9425f66bff3618eeb8ea0fa48789dea8715e7f2cc598aafc145a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909e393deaae408fc3b41edb2a8ab7e1c60d9829c199ab0b73b6ef3527e54b3a`  
		Last Modified: Tue, 19 Aug 2025 03:52:07 GMT  
		Size: 143.5 MB (143542112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833af4e297e61ad6b7d9392f5ba1e0d4b1de2fb80601856d8840e3385a3d8725`  
		Last Modified: Mon, 18 Aug 2025 17:06:20 GMT  
		Size: 80.9 MB (80913624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eefda882742bf56628c372f2ab5d0086a9ecadbc220c33e22a05c5e7555a5c0`  
		Last Modified: Mon, 18 Aug 2025 17:06:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95a64a7f0adcd5161c6c648f86947554e8af31172b1efe2de46deaff1ab6d11`  
		Last Modified: Mon, 18 Aug 2025 17:06:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1561-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:94460786c986adff57e36e1f5dec641ed0144788127c3705677406f658c376cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e36c77275bb690739cd40b324fa34931928dfb55a73f9b63c65fd2594d23fa`

```dockerfile
```

-	Layers:
	-	`sha256:f510cf0a9e4cdee06a688494b3ef626642cdc42410027b66e3d73c7a4056d418`  
		Last Modified: Mon, 18 Aug 2025 18:37:23 GMT  
		Size: 7.4 MB (7374060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf64f93a08538f5578137326e9c709f1271fe1bb0a2d33be48b19829cb7218e6`  
		Last Modified: Mon, 18 Aug 2025 18:37:24 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1561-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:6b259ff788170df50bc95fcfe086c8337f5242ab9fc46b23a079d19dc44a87e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283581091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862a833ff7f4351080f8f72bfca403c92dc93cade90cfc4532f7c978b3d990ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ffad487e544c77a0c7de7f0d0d5d00c797145afe37087c25e8c9d92f650b6e`  
		Last Modified: Mon, 18 Aug 2025 17:16:35 GMT  
		Size: 144.4 MB (144372796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b3441bcd9280b8a5ab7a5cb5307019e3ac190333b0924d751857cdbdcd5cd9`  
		Last Modified: Mon, 18 Aug 2025 17:17:14 GMT  
		Size: 86.9 MB (86869174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448ce8d9647cedfb62948037fff3d2a545f46dc58445a10b0fbf92a1e8ffd3ca`  
		Last Modified: Mon, 18 Aug 2025 17:17:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf692b0a3701016d621c4cab2a7b6c80539463f62634481d9ce63cdce7403f6`  
		Last Modified: Mon, 18 Aug 2025 17:17:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1561-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c3d7fd930cdd11c7e84725b90479113bf1eca0d87d1a53933fe01f38ffaef701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91776a28fd79816fc2308957ae32b8fcacfe08db6ca1d72f7f281279d9ef67a1`

```dockerfile
```

-	Layers:
	-	`sha256:0f7dabb5c5b065884bcde01039d8c0dd44834bda3679055d628f55fc01adc0f2`  
		Last Modified: Mon, 18 Aug 2025 18:37:30 GMT  
		Size: 7.4 MB (7373501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c86e11bf608b7afeea9edd0dc33512a364022dab5dab35f7a9dcb4327dc402f7`  
		Last Modified: Mon, 18 Aug 2025 18:37:32 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1561-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:6a40e3475a07662c545b32b372423053753ddb69747ce85d855937ed1c1382bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.7 MB (261724549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b692f1772742d0483179fb384f31f7e339e8abd8ec5354719f6e4c9253b29615`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965fc491c1e3266f9106d3cf6129a94088b309c79bb586330bc19c70b371f92d`  
		Last Modified: Mon, 18 Aug 2025 17:35:06 GMT  
		Size: 134.7 MB (134724418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787878dbbc0ee4ba2b1ce28be4ee7804fec1bcba47655a326b15114aa9ddbdac`  
		Last Modified: Mon, 18 Aug 2025 17:35:05 GMT  
		Size: 79.8 MB (79849221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8c06cad03e19b2889067fd4ddf8c5d914c26147bc1440f8827da5547b2ad2b`  
		Last Modified: Mon, 18 Aug 2025 17:37:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4048e2036bd8f76645a061624af5915ce2834ba3051d70852a34a3edc454fc`  
		Last Modified: Mon, 18 Aug 2025 17:37:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1561-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9eef4123c19e4e9876ff870f2eff0f7971ea96cc8442e28087d56ed92cbbc4e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7375437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed7dca8af6fd6e5ea6f34b6257ed823e2d11f396fef7e4872ed67dccf50eee9`

```dockerfile
```

-	Layers:
	-	`sha256:0fd41802f1b76fba0ee4b243891506743f2d9c56a45ff3bb3e13c5b9ea0aee8d`  
		Last Modified: Mon, 18 Aug 2025 18:37:41 GMT  
		Size: 7.4 MB (7359616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586f2b013cae1fc657dfd80d4d3986201f19292556143c2041f6c03ad3814160`  
		Last Modified: Mon, 18 Aug 2025 18:37:42 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json
