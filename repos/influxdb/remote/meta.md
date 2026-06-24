## `influxdb:meta`

```console
$ docker pull influxdb@sha256:db561f3dd8656d8f41518a347f3a567ab1760ba3f18f3692d4da583c55ad0cf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:effcd8dd4e08679209cc7c6f6ab0cdf415cbfa2852831a3f35e3ba7f7fc0bb1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91932018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518e6c946da38e5edb12ae4e8dd1ca20cabd7995ad994965d934d1be16e13d91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:41:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:33:33 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Wed, 24 Jun 2026 02:33:33 GMT
ENV INFLUXDB_PR=
# Wed, 24 Jun 2026 02:33:33 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Wed, 24 Jun 2026 02:33:33 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:33:33 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 24 Jun 2026 02:33:33 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 24 Jun 2026 02:33:33 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Jun 2026 02:33:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Jun 2026 02:33:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Jun 2026 02:33:33 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd7bf6f6036613e20f62549df75ed694b99118002358bea5a81baf3929d1ff`  
		Last Modified: Wed, 24 Jun 2026 01:41:33 GMT  
		Size: 24.0 MB (24044046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36dc2d69ffc787189f93daab7cf747b5c7c08e96c86da8df822a14da9b249907`  
		Last Modified: Wed, 24 Jun 2026 02:33:43 GMT  
		Size: 19.4 MB (19385194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17f1d276670c0a1551e05792856eed717d8541b7ed54ddb4607f2fce6ad3737`  
		Last Modified: Wed, 24 Jun 2026 02:33:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5be5f0deb279a81aefa1f3b4d90a0c1f1b8a2f146d04610c04e5d4697cd317`  
		Last Modified: Wed, 24 Jun 2026 02:33:42 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:e173c53c430e01e9dcc738b385cdbc137897b7ab0236c1cf54023c5707fc32dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a762acb43a2b7c7c001d605190ee5743c3463c91adcc29fbcd41b33f218420`

```dockerfile
```

-	Layers:
	-	`sha256:fee72c9f216a11ade21112b2b13992e2211cb338c424657673d10f218f24d6d5`  
		Last Modified: Wed, 24 Jun 2026 02:33:43 GMT  
		Size: 4.6 MB (4593227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c04e4b31cff2eb708e83c3dc193382eac26eda7bad16ae41cf1a80bdd62fea5a`  
		Last Modified: Wed, 24 Jun 2026 02:33:42 GMT  
		Size: 12.7 KB (12664 bytes)  
		MIME: application/vnd.in-toto+json
