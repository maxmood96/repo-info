## `debian:stable-backports`

```console
$ docker pull debian@sha256:ed3fa9bde03cc5180f9ed7570e0c4478ed57ec2aa518e516ccfdcf7e93167273
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:da980cebfb4383a4892a2f95b62b233103234b8a29d6c059f45fa1eb1fe848f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49284851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a687df0c30a835d3e035814d00d5fdf501d2fcaba3296c97853a9e3bb48259ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a1d865bc2cbc03af4eecb96149727facea254a73137e774f5041eecb07a31f52`  
		Last Modified: Mon, 29 Sep 2025 23:35:22 GMT  
		Size: 49.3 MB (49284631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655f6476d7b7b24b618ebb7267396d788e0694e566d9bc2d893435f5fdbf9dd7`  
		Last Modified: Mon, 29 Sep 2025 23:47:08 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5b8ff1dce9a1855dc773061aeb5342bfc2f90bd6dd546314b06993636dd70d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98436aabcc1d723970f92151bd7967f07486041303f9cc5a57ac7eae5df1198d`

```dockerfile
```

-	Layers:
	-	`sha256:179dae4cd0bfb263f1267b67ab8d01c071b6aa08b459d613813a3d98b4bb564f`  
		Last Modified: Tue, 30 Sep 2025 00:30:31 GMT  
		Size: 3.2 MB (3169970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5759f94ddc731721ea331f042f8899d82b216614c13b0263b4ed6e971b29035`  
		Last Modified: Tue, 30 Sep 2025 00:30:32 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b9f8c6005d4c77157056a81b026fdbeaa07f478a4638cc041ee49fc60957b8b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47448701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7c0d48b5b1f3eea0428d67e9ccd7fe77b3ed54d2377db9ebd2c04f71e5a176`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9ef504d95b114e66ba49aa84cce79d6d366bcc384feac920fd40b3f60e6684fe`  
		Last Modified: Mon, 29 Sep 2025 23:34:11 GMT  
		Size: 47.4 MB (47448480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262b4b0bc9bf67d97f673edd0d5adc4f7a6772c38297a9733147cec9ba7683f7`  
		Last Modified: Mon, 29 Sep 2025 23:52:02 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e9c5500677d8cd6a3904e935844a5de092c928d3fa8abe25d9ef51c9d5fd1844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc139c6817bea1e64d667dba5cced5d9576e92d3e4a994b606645741fcf86af`

```dockerfile
```

-	Layers:
	-	`sha256:0c0e4befeda31fe8cf81239bb607e62266d1e318e217c4ec4b94b3c89deebec9`  
		Last Modified: Tue, 30 Sep 2025 00:30:37 GMT  
		Size: 3.2 MB (3172907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ca655f41dca28159668f2c050d5f1c72ed526366b77a98a99b95f88dff2b39b`  
		Last Modified: Tue, 30 Sep 2025 00:30:38 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:0e2434fe5b7ef98eb802afe746c7e5137ad907cdfb97e199cc72d5a66ad5e356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45716361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40fda7cb9c8c99757663d47c2c5159506c749305a613f83d5432e5535cd4c4a4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:dd26cdedcb5a26641c601cd55df184a46de3242898466351fbab2e0a2e910745`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 45.7 MB (45716140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6010e3934f8e4f740ec82fe7b2a6ce5c01a0a1c78efca8ee32edd71c1b8a836e`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d974ac1f9df18be7633292bcf007108328d6e7874a1fb095d5e1e9d7ad9f7ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfdfa778a3974e52ecd20a0ecf5698223cd5000c5005c7793fe1f09bde56121`

```dockerfile
```

-	Layers:
	-	`sha256:bc372be43b0e63066610bbc6469bf540e62967bb8d350f3115671c111354fba5`  
		Last Modified: Tue, 30 Sep 2025 00:30:42 GMT  
		Size: 3.2 MB (3171344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c479d981026725f1cafc31eefa6a7526822f9bfe63c2665829956d5618ef3f64`  
		Last Modified: Tue, 30 Sep 2025 00:30:43 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5d67c95b97712d8af9c8fedf03ae7dcc0b8c567fcc984b14fdfeb7cdab846f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49648918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e794e3d7058b0c37258844950d458d3d3ffd443e16b7d4c5c1b66f11367ceea9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ea1fb054c1694119de48ab87827d654b58de87d7b24f19b97f20bceed0351589`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0783ef4a35c59afa669ac4e7d87987d90ded2e8a21157c1c74f9a095c3d451f1`  
		Last Modified: Mon, 29 Sep 2025 23:48:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6e91fbfb01fe995e674fbbf662451928e0f8a34a0868d00f3e1fd05cc3ab422d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9811cf3f4c439a16e8b4b98547cf50a3234f5cee0d3e6aabfbecdf88a69d2290`

```dockerfile
```

-	Layers:
	-	`sha256:ea149fe9fb08ff1976ee49bd9540e88a0565e5714dc2340599c2fe8cdf2fd0ee`  
		Last Modified: Tue, 30 Sep 2025 00:30:48 GMT  
		Size: 3.2 MB (3171451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16e9ab51c2eaa643a0e181c254b72ca5352bb1f91e0797ce6c5ebf8c56647b7a`  
		Last Modified: Tue, 30 Sep 2025 00:30:49 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:2c5a1a3357aac8ea5e96a734fe731780021cc4855e67980cf5807b1545436323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50800448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93632df1cb8e14a167581dbc9fa5613e6a02bab6a5f22f73347fa9012ab6550e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:04c256590493e5279994c2b667347046decd878edb6c369fa049519209f18f21`  
		Last Modified: Mon, 29 Sep 2025 23:35:31 GMT  
		Size: 50.8 MB (50800228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66890eed937553d683336c68e5ad39212773f224702b61f7a097d884705b417`  
		Last Modified: Mon, 29 Sep 2025 23:47:20 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1d42888945865ac8392cc59a8daaea8ec8f3ff3f1578768a9fabf400bfef6199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694dc726c4f8b9539c432080fb666de28354e1b4ebc46b2ea71eb0966df1a1ae`

```dockerfile
```

-	Layers:
	-	`sha256:0b6de5c9440b16270aca8235f6036d3f37a95a6d4d6fa3bd9766ab69aa97d57d`  
		Last Modified: Tue, 30 Sep 2025 00:30:54 GMT  
		Size: 3.2 MB (3167173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04e34a6328820ae22720f984477dd6ad0de1e4de8ef4aec3e6882679e312c5ae`  
		Last Modified: Tue, 30 Sep 2025 00:30:55 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f9ba46b966fe65877fa0f45ab3989c70246cb5bcaaacece68a2cd633f3872d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53109436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665fc603ed435e96871f967e04fac73c02089159adfd9e5943609f57ccebdd2a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3da8db40e548c1daec12a4f84731c6b23a4314bf13bd680b12a5326ee930bf0b`  
		Last Modified: Mon, 29 Sep 2025 23:39:20 GMT  
		Size: 53.1 MB (53109215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096708b3c2c9293a84315f0a9d1c2b230d42bdcef2548864f60393c6c9321d9`  
		Last Modified: Mon, 29 Sep 2025 23:49:21 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2965ad86b46d416d2888d8082c61ec0a0ed223d4bc7679b227382c9f8dae63df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee07767c029233934e457ce351ca5d05f01a0a68016c9131cfef44b2f584cbd5`

```dockerfile
```

-	Layers:
	-	`sha256:333b81cc9046e0ddfdb30dcb4bbf0c091e2d4e32547a9f42b70f2851b3abbfd8`  
		Last Modified: Tue, 30 Sep 2025 00:31:00 GMT  
		Size: 3.2 MB (3173481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:201d7496b27cdc19a17f397ba601e1134f1911296029746dd630ed566f6650a3`  
		Last Modified: Tue, 30 Sep 2025 00:31:02 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:11a2711234d69eb5c1ab50a2deab36806eee5676cb881d810347272b7a87c51a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3215a2fa26e2a6116c153c7ea159a091d62e2d95ead7642a4d7974942ecd2815`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:52f33c04e7c9496cede0fc2b22eeb9e3106d36bc88f737aac31381e17eb9914f`  
		Last Modified: Tue, 30 Sep 2025 00:56:37 GMT  
		Size: 47.8 MB (47770007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a350237bfc8d5df28818aca1af19560b56733a91a387dd24ce54b202f0930906`  
		Last Modified: Tue, 30 Sep 2025 01:25:19 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1f120e3e7fca60fe0372862cd1c2ebc5350b35b2d16e2c8116a56106cd5231c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3168146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42564cf82597c92784dd2f03804882d438c05d704d8911ec8e96e5430d511156`

```dockerfile
```

-	Layers:
	-	`sha256:b45e653b6078e5beef927bd90ab37e1a6c43d61ca349eaeaa741febbc5418e18`  
		Last Modified: Tue, 30 Sep 2025 06:34:21 GMT  
		Size: 3.2 MB (3162293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97fc06347f880aa6dc8c38878cc6ac6d09a8c3a29e7eac452b02483b74988fac`  
		Last Modified: Tue, 30 Sep 2025 06:34:22 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:6c0451e9b8c8418f770f26fbbca203c9bd9e1b90f9c5e98b6b78bef5a36360fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49351663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5129bb26cf9fe577f381f399c4b39cb9389cbc7c22a3d82ae1f4baa63b95fa35`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e70e4854e6e6c799ee27531f422fa0035bb084497fd35302da9693a931b800e5`  
		Last Modified: Tue, 30 Sep 2025 00:46:31 GMT  
		Size: 49.4 MB (49351441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737521eb8a3caf3dd4487e7f0647f4d7a0d4f75b54be7af0bd757053cbd36f07`  
		Last Modified: Mon, 29 Sep 2025 23:47:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8bc4a57911dd3dc68ce8f3bfd9211d92f1e0a417a29c33e10b6d47267cb1dfa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e5d408e3402153dd0f130e2295eae0d5c5b19ed6ed7c1486b417beafd68425`

```dockerfile
```

-	Layers:
	-	`sha256:3e1709af8611ddbccc03b73e086acc24583397669efe75bd360545720f301768`  
		Last Modified: Tue, 30 Sep 2025 00:31:10 GMT  
		Size: 3.2 MB (3171417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dca8996ebf508cb9302c2c9e6f4d2065705e2ecfc9123b7c20cb1b1abed27ea4`  
		Last Modified: Tue, 30 Sep 2025 00:31:11 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
