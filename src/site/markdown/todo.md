<!--
  Licensed to the Apache Software Foundation (ASF) under one
  or more contributor license agreements.  See the NOTICE file
  distributed with this work for additional information
  regarding copyright ownership.  The ASF licenses this file
  to you under the Apache License, Version 2.0 (the
  "License"); you may not use this file except in compliance
  with the License.  You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

  Unless required by applicable law or agreed to in writing,
  software distributed under the License is distributed on an
  "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
  KIND, either express or implied.  See the License for the
  specific language governing permissions and limitations
  under the License.
-->

Todo
====

### Index Pages

* check consistency between team information in [Maven parent pom][1] and in Apache LDAP [maven][2] and [maven-pmc][3] groups

# Done

* See where to publish the result on Maven site
    * jenkins site URL https://builds.apache.org/view/M-R/view/Maven/job/dist-tool-plugin/site

* take screenshot of site. ( os specific )

* Separate goal to fail the build, so we don't have to check the report daily, but let the CI server mail when failing.
    * notice that failing the build will make the report unusable: so we must have either a separate goal or a mail sent explicitely from plugin
    * there are some known issues with old artifacts, which don't have newer version expected: need to configure these as "accepted exceptions"

* dist-tool.conf format as a DSL to organize distribution area check rules

### Source Release

* add date of release (from artifact metadata)

* Check older artifact in dist (only latest should be present, previous version removed)

* Shell command for cleaning older artifacts

### Sites

* add date of site
    * [sky] date from comment part in skin (not always ok :( )
* remove "check if version present", since our inheritance ensures we don't have problems
    * [sky] kept only for precise layout check
* replace Skins columns with one unique column "Skin used", showing which skin is used (with version)
    * [sky] no garantee some site like http://maven.apache.org/plugins/maven-one-plugin/ have no style header 
* add date of release (from artifact)
    * [sky] date from metadata is ok ?

### Index Pages

* Check if artifact versions are up to date in listing pages:
    * http://maven.apache.org/plugins/
    * http://maven.apache.org/shared/
    * http://maven.apache.org/pom/
    * http://maven.apache.org/skins/

* support different dates in artifact metadata and in index page: it's consistent if difference is only a few days
(date in index page is chosen by the release manager between the vote start and announce)

[1]: http://svn.apache.org/repos/asf/maven/pom/trunk/maven/pom.xml
[2]: http://people.apache.org/committers-by-project.html#maven
[3]: http://people.apache.org/committers-by-project.html#maven-pmc
