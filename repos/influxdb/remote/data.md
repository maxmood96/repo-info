## `influxdb:data`

```console
$ docker pull influxdb@sha256:e6398d43e07f280786f433bf80f8639b750bfb50e5c747ffc4ddc9e2a60c5b7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:0f1cd7dc2417b33893cf37d0c221c1d141fea39c7e6f3d75987d2ce2f39c7379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115722571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e946c6558e16f25290a65d9cacce4a62fb96fa1e024c32df5af02a52dce8e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:41 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Fri, 08 May 2026 20:30:41 GMT
ENV INFLUXDB_PR=
# Fri, 08 May 2026 20:30:41 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Fri, 08 May 2026 20:30:41 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 08 May 2026 20:30:41 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 20:30:41 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:30:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:30:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 08 May 2026 20:30:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:30:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962acf40db3a7d5df88755121d66b97b074e6fa7af51182c3582c3fbb65fdfb2`  
		Last Modified: Fri, 08 May 2026 20:30:56 GMT  
		Size: 43.2 MB (43189938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcb508adabb85feb56df9db23493b1b85833909a099c96a55ee681b41293c99`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f6c1227d43a6d82ff41b8ef79cb08bab47864e59f8c6884a2a263d146821d3`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db63a3ea8649aa33914a2860a788be1b9e77252249952311c7ba20c888f8b43`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data` - unknown; unknown

```console
$ docker pull influxdb@sha256:3a80b17123ca1905ae253c10601c1a1906b0f118b45e3254adebf76cc7782238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a478a44f1e471ed0a0b7184d1ededb0817c5a7f997b34f0fa4b76f3cf8b5003e`

```dockerfile
```

-	Layers:
	-	`sha256:43aec9720ab4169c00241c51f14a8db53355c107f19b19a1e1fc4897ce1db8b8`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 4.7 MB (4693123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c013f1c88633b1a08bb7a4ffa1463dd4ac279bf38bfb418977e5426907519d6`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json
