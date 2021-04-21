## `influxdb:data`

```console
$ docker pull influxdb@sha256:4c7a72ba2fe0220693f98e7625d71c0575072b0e8de5846fd3d6aa6ef19328bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:dda796abc4273a9677f168468a5a4d354768aabbc8649123f5a5c9752041fbab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127762482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3251fd11a122e84b730fb89fee700c1d9ebe4484bdfcf05447bbe2be44ad6424`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:41 GMT
ADD file:e3d37689e896a83d39040f2c95091ff88f3899b5b410dbf76908dd6c938b8cb5 in / 
# Sat, 10 Apr 2021 01:21:41 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:57:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 19:13:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 20 Apr 2021 23:26:48 GMT
ENV INFLUXDB_VERSION=1.8.5-c1.8.5
# Tue, 20 Apr 2021 23:26:55 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Tue, 20 Apr 2021 23:26:55 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 20 Apr 2021 23:26:56 GMT
EXPOSE 8086
# Tue, 20 Apr 2021 23:26:56 GMT
VOLUME [/var/lib/influxdb]
# Tue, 20 Apr 2021 23:26:56 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 20 Apr 2021 23:26:56 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 20 Apr 2021 23:26:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Apr 2021 23:26:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:76b8ef87096fa726adbe8f073ef69bb5664bac19474c5cce4dd69e08a234903b`  
		Last Modified: Sat, 10 Apr 2021 01:27:52 GMT  
		Size: 45.4 MB (45380037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2bafe8a0f40509cc10249087268e66a662e437f10e9598a09abb5687038a57`  
		Last Modified: Sat, 10 Apr 2021 02:04:34 GMT  
		Size: 11.3 MB (11286411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53ce1fd2746e8d2037f1b0b91ddea0cc7411eb3e5949fe10c0320aca8f7392b`  
		Last Modified: Sat, 10 Apr 2021 02:04:33 GMT  
		Size: 4.3 MB (4342420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411d661fe5a6d03bcbf4c331f5baa050071efd4e152404ba66693d31e11177a5`  
		Last Modified: Sat, 10 Apr 2021 19:15:58 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39542ba36788d3c1f4fd8c99f3c8ee60bcd516988ebaca5c7f055527f0bd0986`  
		Last Modified: Tue, 20 Apr 2021 23:29:05 GMT  
		Size: 66.7 MB (66748986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34760563a3eb357904f49e882eb61c406ae738b0c725be9a5b8de662a6439d2`  
		Last Modified: Tue, 20 Apr 2021 23:28:53 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc95cb561e08ad735f4d3999ca6f231a24c951fe303c3b007862a688141674a8`  
		Last Modified: Tue, 20 Apr 2021 23:28:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04edce497c0761075c347d6f71dfa8666e3180eec1bc8d7f21d200b24ca105f9`  
		Last Modified: Tue, 20 Apr 2021 23:28:53 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
