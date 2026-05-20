## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:4ac1dac0e04bdf79a3ff3bcc818e7fe55710f96dee27f75d208bcde00a46eab2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6a248e47fc6c41b2d950d69e3c0dee1802b5171d46724393a7ea13a521689fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281538972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8191e66eda8d979ee21ef97c7150adb0fd41de994cca36b0dc39a52b00908e3c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:00:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:00:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:00:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:00:11 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:00:11 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:00:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:00:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:00:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:00:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:00:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4851a5062821afcb326424b5796a4fd2f71a95b396db1fe9a569ccd202e39e`  
		Last Modified: Wed, 20 May 2026 00:00:47 GMT  
		Size: 158.2 MB (158166903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0423bcd387e978706bdbcf32fffc2322db37a6338ecfe7fcdd89813d54c98e6`  
		Last Modified: Wed, 20 May 2026 00:00:46 GMT  
		Size: 69.6 MB (69602173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5de8d39c5e5e216f72a0df4c20488bdc2ab7082ed154ef7a385b4279f946ad2`  
		Last Modified: Wed, 20 May 2026 00:00:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2832e3e50089112642af584c04b6000d5d1f5700120da9d7f5ded5edaf15eec`  
		Last Modified: Wed, 20 May 2026 00:00:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:aa808195b4caabe415850895b0250b38d583a33df7568202f4aa2f24870b0dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7426062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d735eeab1b97d4bc191e5f158894ecef66f23ea9f17eaa4d4fe8c6e130b335f2`

```dockerfile
```

-	Layers:
	-	`sha256:0cc9076c2c0f4101eaeeb13ed8cd0c18c1ba3f11c25e5f09991449c47982386c`  
		Last Modified: Wed, 20 May 2026 00:00:42 GMT  
		Size: 7.4 MB (7410130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fa44523a8039d5463b29388b64bc3ba6642cbb39a7266f2b401478a1130d34d`  
		Last Modified: Wed, 20 May 2026 00:00:41 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d0567e6ee83245e6a994f9a30580058f734053aff7457542cdc6d3f56dbaaab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278489777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548d0d6d76e95c61860782d2fe350ef6d12a84b9bb444abbdbb381896e6892b0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:07:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:07:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:07:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:07:23 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:07:24 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:07:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:07:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:07:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:07:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:07:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760bba207f1e657b1d3f69b9b383f06e8c76bcf72b09e0d58621e6a3032d58e7`  
		Last Modified: Wed, 20 May 2026 00:08:04 GMT  
		Size: 156.5 MB (156461285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ceb1f526f6bc01be96bc4a9ffa881e06040b7967269813ea7f1a40d4e4a671`  
		Last Modified: Wed, 20 May 2026 00:08:03 GMT  
		Size: 69.8 MB (69770871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbbb99c2409fd201bc1bc03de1d7acac217092c8022ea166f59c6e79809b464`  
		Last Modified: Wed, 20 May 2026 00:07:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2c28ce1a37563feab88ff6f1f7edbba8f9b5a5cc5f60792e5d63ce2e9f5247`  
		Last Modified: Wed, 20 May 2026 00:07:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:83c1d4f0a9b8cd9a7dff7789c18498de332ef6edb21667b873b88805a3331842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7431279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d3f4fa04d6c500b78cefaf2fb28983542cfa64f71cc9b342311766168c1e40`

```dockerfile
```

-	Layers:
	-	`sha256:61ad5ef1fd620705185aad35d17d36c4f37de3b985482e36ba0ddff22fb9590a`  
		Last Modified: Wed, 20 May 2026 00:07:59 GMT  
		Size: 7.4 MB (7415229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b7391574b0cc6e607bc6256b82832193aecd91f425665991b1baa5106a5eaf1`  
		Last Modified: Wed, 20 May 2026 00:07:58 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
