## `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:ad82d552dc9689ca349f5895d87e4ced90beedd4b462ecfed44fd0385b413e7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:83792ac8d574d0fcd1f029ebea8b7f0fff7e499909782f451b433ec238625b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255320290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25300c196035b733a4fbf80e19f8ad68347f6ff58f46abe39d749c3e2e093f10`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50281334d943ea178c902708c0f10f4a5adb18ae738768657d99962d0c2d8b21`  
		Last Modified: Mon, 17 Mar 2025 23:18:15 GMT  
		Size: 157.6 MB (157585931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c55c51eb709350074fde2403a3833c9664ad9a9799fbf139b87f20f7091fa7`  
		Last Modified: Mon, 17 Mar 2025 23:18:12 GMT  
		Size: 69.5 MB (69528456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62220e96caa4c36c67d7879049746146b7a01a9737ada879ef5072709d5a6476`  
		Last Modified: Mon, 17 Mar 2025 23:18:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1be7da784f37bada63c54f24403f814ad3380f005f1633326434aa9a974901`  
		Last Modified: Mon, 17 Mar 2025 23:18:11 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2a9be6b7c95b1ec79031c50630da7973134bd45b79312662b8eaed465b1d1c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57eb86f4a56ec36aaa9413079abfa8c6a4dcd896f6241055e434bbe7fa9a80bc`

```dockerfile
```

-	Layers:
	-	`sha256:d2a18d462cabb75031789cda65fafd9c3c26a65a8d34ad3c5eda2cc9c87f3b3f`  
		Last Modified: Mon, 17 Mar 2025 23:18:11 GMT  
		Size: 4.9 MB (4916395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e87e7143afb9674234a6252e01cae3149cb813442e18e13b6f07092a2d91567`  
		Last Modified: Mon, 17 Mar 2025 23:18:11 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:79b65658a5777aca0448f664e01d9ea6bdef7d458bfeda5005d42411e9420dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.3 MB (253281917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293ec116b8bb45cf777536253b2c572e68f2a1f52ea48544321e9d5ba28599e6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb57ba6e2b02f933ad614475b6f0f15a4ad1d07504d61cfdc82617f99c428209`  
		Last Modified: Mon, 17 Mar 2025 23:49:19 GMT  
		Size: 155.9 MB (155859251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa805c91e54c462fec6302e8866098be6489f8ca6624bc22861ee1c5e1f5f890`  
		Last Modified: Mon, 17 Mar 2025 23:49:18 GMT  
		Size: 69.4 MB (69377589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41fac8811e6969d541dbc2d8fc508a95e59c8e2d79eef92774b0d9eb9d0fadb`  
		Last Modified: Mon, 17 Mar 2025 23:49:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80f3b38cb0a48573f67fb1b82af6da0ec79810531df44c6478f02bba3018122`  
		Last Modified: Mon, 17 Mar 2025 23:49:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:053d934bdbe7b1503d13b0bcf82511227a5f177015103c80a2b89fd5ccdb8e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee86154d473fa27c612dd5a9cb4641df1f70fdf135bae0fe0a0a941e05d8268`

```dockerfile
```

-	Layers:
	-	`sha256:44af36100606eda8c14d28f32164506c31f027e7e110b5e3bbafb2be3b23d40a`  
		Last Modified: Mon, 17 Mar 2025 23:49:16 GMT  
		Size: 4.9 MB (4922180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:005d98ff02d4650ee4242ddade0a1c069568dc3d13a72d37cae0115bf93c48d3`  
		Last Modified: Mon, 17 Mar 2025 23:49:15 GMT  
		Size: 16.7 KB (16716 bytes)  
		MIME: application/vnd.in-toto+json
