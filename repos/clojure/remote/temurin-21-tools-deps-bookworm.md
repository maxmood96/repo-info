## `clojure:temurin-21-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:84fa2b90f77932959932e38d863e8a6bfa4e073e3030d05482e10336b84c6f94
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

### `clojure:temurin-21-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ca3c82998fb533484489909ce156901aed93f72cf006a9b371fcc19d5ecb249a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284795326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c0f3922660de005318f32dbae5def5a9dd82ecef1b3622bb772a4c8f061f90`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:19:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:19:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:19:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:19:29 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:19:29 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:19:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:19:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:19:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:19:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:19:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678d4591ddcc28de0689396e5190b8728ee8f8b9951d3120627b4ce7a5d2836c`  
		Last Modified: Wed, 24 Jun 2026 02:20:08 GMT  
		Size: 158.2 MB (158166926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304180bfb0f23cca96c83f33962abae0aca3b4eb87207e3658d6a2c74dfb8220`  
		Last Modified: Wed, 24 Jun 2026 02:20:07 GMT  
		Size: 78.1 MB (78125149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b120762c49493788fa7c81155a70978e8af3abae7f3ce717067c0d3f29121a3f`  
		Last Modified: Wed, 24 Jun 2026 02:20:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72763c93e07505462fb33588493414ec7a4a43e15abb115331c9f0ad2c53349c`  
		Last Modified: Wed, 24 Jun 2026 02:20:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:21902bfc1d9a9b95f28c52b1be2e79641c22fe8424635a5cefcb90bd68a2f215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f00acf09f8be5a96813e7f40853d228533a22c77b3be4ca5b7d67609b50cda`

```dockerfile
```

-	Layers:
	-	`sha256:b02a9bd03b83c560a8d952df7d6f847448b5bc875184349afa2c5eb2b8c00071`  
		Last Modified: Wed, 24 Jun 2026 02:20:04 GMT  
		Size: 7.4 MB (7378670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7c5b6488e4a4cbb9954ba3fd844b7b733a4f631b0ecb0384a6bbf0c8fe72a2`  
		Last Modified: Wed, 24 Jun 2026 02:20:03 GMT  
		Size: 16.6 KB (16615 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:218469e3a10d0934fce88fee63ddd2dd902b31c0ab1be200849683155517918b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282981351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea66e7c806f2db92f5cd293a1ec776f51791d550ebb121f88a71608c6638680f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:25:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:25:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:25:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:25:59 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:25:59 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:26:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:26:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:26:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:26:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:26:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f18aefff1f7a59c8b8b4356d25fee763811f17dc1e1a63105c46349ca6cc016`  
		Last Modified: Wed, 24 Jun 2026 02:26:36 GMT  
		Size: 156.5 MB (156461287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e386f1ee2b7813fd916ec026f0cfe881b68d15329efc35304841a2305b61695e`  
		Last Modified: Wed, 24 Jun 2026 02:26:37 GMT  
		Size: 78.1 MB (78129822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bc8dddd144e8025c47a187391808bf011c923052f39c3b18d10e3225b02c2e`  
		Last Modified: Wed, 24 Jun 2026 02:26:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257d1f24172194e7259c15a6cbd5e200774f9bfae56b60bbc7bcdaae052c53ca`  
		Last Modified: Wed, 24 Jun 2026 02:26:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8a74fe8eb1b0942693601b44c6cead004d397f5eb5891ea7900f571c22f53308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65af1b82b847fc2c380c7862ee2329f66c88af4d1a66f66f9261dd76b08a405b`

```dockerfile
```

-	Layers:
	-	`sha256:03a13f312863af3a9c8a04f2f82225b086004231647c29afe56405ec97b4c93b`  
		Last Modified: Wed, 24 Jun 2026 02:26:34 GMT  
		Size: 7.4 MB (7384457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b512e4c6eb1c559896e13475a3be522564f0cea11e7acbdbec16b1f5480c1b1`  
		Last Modified: Wed, 24 Jun 2026 02:26:33 GMT  
		Size: 16.8 KB (16758 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:5790516c33246f0ae3f87ac19bb2dd56cc8483a5c34898dac31789c6c7497510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294649537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba940732e6e5be1e719ae447a503097f17c0f0caa3e6fe85107530c7281a00eb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:52:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:52:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:52:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:52:36 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:52:36 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:51:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:51:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:51:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:51:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:51:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2baefaed51aa669676a6ca72a1976a52e2ef31d6ede3f6e16283490f461501`  
		Last Modified: Tue, 16 Jun 2026 23:55:52 GMT  
		Size: 158.3 MB (158343250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c76d4606a4fdf30a370796d0ae5ce1d68f7eb31023418b1bdc61dec65a42fb9`  
		Last Modified: Fri, 19 Jun 2026 02:51:49 GMT  
		Size: 84.0 MB (83958581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7437237bf82753108a524dc96421224eefb13579517ad60befe7f4d018c188a6`  
		Last Modified: Fri, 19 Jun 2026 02:51:41 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b24fb6e9645776f5efc2d1cc8924ab2688b027e5cb7462b8cb788c684c07a5`  
		Last Modified: Fri, 19 Jun 2026 02:51:41 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2ff0cd7d870f50916842f6674bbd42fbc4c6dec1aaed3a85aab9b6a09790502c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c409d19986f62cdcd358db789918961840d46e63839414e7f665278ff9e2fc7b`

```dockerfile
```

-	Layers:
	-	`sha256:d428336e5aee0054ab23ea93695fc1fc8b8ed56f6eec6f8a5cb688224725899d`  
		Last Modified: Fri, 19 Jun 2026 02:51:46 GMT  
		Size: 7.4 MB (7383898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ea0761faa926ec3409fd6569ce404a70ceab89e92922da36fc19a794f97029`  
		Last Modified: Fri, 19 Jun 2026 02:51:46 GMT  
		Size: 16.7 KB (16675 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:db187308878735259139201c24a7701439a99d88c5b9cbcda4c6cc99292ab1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271480110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df5a16044854cd676bd9bb8c2449959e3f1526b82745a45433f3e707b2d8bee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:36:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:36:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:36:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:36:10 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:36:10 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:20:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:20:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f3439d92caf07670440a960bb879707c16dc5e881fbc688c4e1a643175e72b`  
		Last Modified: Tue, 16 Jun 2026 23:37:41 GMT  
		Size: 147.4 MB (147388366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b725c67439d0a7c5a177afc011e08bf5b3f71366b0f05785fa067eeb2ac1be0`  
		Last Modified: Fri, 19 Jun 2026 02:20:35 GMT  
		Size: 76.9 MB (76929207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451226aff33c9198bd7b5b4cf659de5ccc89cdc6c6b10605251e6c1058fe6533`  
		Last Modified: Fri, 19 Jun 2026 02:20:34 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6849a0ddc42c6660f680465fbdd561f409dca81e0f2e3abae45d99ff65eb4ba8`  
		Last Modified: Fri, 19 Jun 2026 02:20:34 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f565b66c527c62d56c020ed262757069522c2b1f76da43316c52f97ad850ab5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5baf26e809df7a803fe98eeda9a1227123d6ed41e9f35e42e5e16e61f22faa8e`

```dockerfile
```

-	Layers:
	-	`sha256:9b8e956bfe957e002f6f9952213da75cd470b0dcf18f9ec0c4fbd3461d4159d5`  
		Last Modified: Fri, 19 Jun 2026 02:20:34 GMT  
		Size: 7.4 MB (7369989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:354dc17860e46c3b9ae84d74b750caf000719c3e48ca9b8035290fb1c99f565e`  
		Last Modified: Fri, 19 Jun 2026 02:20:34 GMT  
		Size: 16.6 KB (16616 bytes)  
		MIME: application/vnd.in-toto+json
