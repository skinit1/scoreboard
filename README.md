	@SuppressWarnings("deprecation")
	private void setupScoreboard(Player p) {
		
		ScoreboardManager sm = Bukkit.getScoreboardManager();
		Scoreboard onJoin = sm.getNewScoreboard();
		Objective o = onJoin.registerNewObjective("dash", "dummy");
		
		o.setDisplaySlot(DisplaySlot.SIDEBAR);
		o.setDisplayName("" + ChatColor.GREEN + ChatColor.BOLD + "SKINIT1");
		
		Score spacer = null;
		
		Score nameTitle = null;
		Score name = null;
		
		Score spacer2 = null;
		
		try {
			
			spacer = o.getScore(ChatColor.AQUA + "");
			spacer.setScore(4);
			
			nameTitle = o.getScore(ChatColor.GOLD + "Name:");
			nameTitle.setScore(3);
			
			name = o.getScore(p.getName());
			name.setScore(2);
			
			spacer2 = o.getScore(ChatColor.BLACK + "");
			spacer2.setScore(1);
						
			p.setScoreboard(onJoin);
						
		}catch (Exception ex) {
			System.out.println(ex);
		}
		
	}
