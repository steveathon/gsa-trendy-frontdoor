# Overview

The GSA is an exceptionally powerful tool, however when you are using it as a primary search destination the front door page is a bit boring.

This code adds the functionality to your GSA to use the power of [YQL](https://github.com/yql/yql-tables) to display results FROM your GSA that are realted to the trending topics on Twitter, right on the Frontpage of your Search Appliance. 

By showing results from your index, you can be sure that users will find what they are looking for faster and more relevant to the current trends on the general internet.

# Usage 

In the attached stylesheet, you can see the following variables requried at the top.

	<!-- *** Google Trendy Frontdoor Integration *** -->
	<xsl:variable name="show_trendy_frontdoor">0</xsl:variable>
	<xsl:variable name="gsa_publicurl">your.search.appliance</xsl:variable>
	<xsl:variable name="trendy_use_testing"></xsl:variable>

You will need to set gsa_publicurl to your public host (not including the http/https).

If you are testing, use the trendy_use_testing as your entities encoded use table string for YQL with a proceeding %20 for good measure.

# search_results_body

In this template, you will see the following bunch of code:

	<xsl:when test="Q=''">
		<!-- Begin Trendy Frontdoor -->
		<xsl:if test='$show_trendy_frontdoor = 1'>
			<xsl:call-template name='trendy_frontdoor' />
		</xsl:if>
		<!--  End Trendy Frontdoor -->
	</xsl:when>

This xslt test for Q='' has always been in your xslt, now we have added an if check to see if you want to show the trendiness.

# Dev Notes

I've wrapped the Javascript inside the xslt template:

	<xsl:template name="trendy_frontdoor">
	</xsl:template>

This is because it was a quick hack. I expect if people find this useful they will make it look nicer.

# Testing !?

If you want to test this and you are not getting a good set of results on your GSA, find someone willing to lend you their GSA or talk to your local GSA nerd.